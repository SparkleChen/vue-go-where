<template>
  <div>
    <div class="weekend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-img-wrapper">
            <img class="item-img" :src=item.imgUrl alt=""/>
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'Weekend',
  props: {
    list: Array
  },
  data () {
    return {
      recommandList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/53/4bcd11cc3a5374.jpg_r_640x214_988a4cee.jpg',
        desc: '自然风光，畅爽大自然',
        title: '芭拉湖景区'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/5f/276ed6784d25ee.jpg_r_640x214_2193082e.jpg',
        desc: '自然风光，畅爽大自然',
        title: '武隆天坑地缝国家地址公园'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/48/f117e9b3bf582a.jpg_r_640x214_b8145711.jpg',
        desc: '自然风光，畅爽大自然',
        title: '乐和乐都主题公园'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1506/1e/f97881dbd07520.jpg_r_640x214_f8c25916.jpg',
        desc: '自然风光，畅爽大自然',
        title: '金刀峡'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .weekend-title
    line-height: .8rem
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
