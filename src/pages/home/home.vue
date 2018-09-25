<template>
  <div>
   <home-header :city="city"></home-header>
   <home-swiper :list="swiper_list"></home-swiper>
   <home-icons :list="icon_list"></home-icons>
   <home-recommand :list="recommand_list"></home-recommand>
   <home-weekend :list="weekend_list"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommand from './components/Recommand'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommand,
    HomeWeekend
  },
  data () {
    return {
      city: '',
      swiper_list: [],
      icon_list: [],
      recommand_list: [],
      weekend_list: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.city = data.city
        this.swiper_list = data.swiperList
        this.icon_list = data.iconList
        this.recommand_list = data.recommendList
        this.weekend_list = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style>

</style>
