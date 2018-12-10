<template>
  <div class="mpw-download">
    <span class="ad-close"></span>
    <span class="ad-log"></span>
    <p class="ad-txt">
      使用去哪儿门票客户端
      <br>
      享受专属优惠体验更流畅
    </p>
    <a href="" class="ad-link">立即下载</a>
  </div>
</template>

<script>
export default {
  name: 'HomeAd'
}
</script>

<style lang="stylus" scoped>
  .mpw-download
    position: fixed
    left: 0
    bottom: 0
    width: 100%
    height: 1rem
    background-color: rgba(0,0,0,.8)
    .ad-close
      position: absolute
      width: .5rem
      height: .5rem
      display: inline-block
      background: #afafaf
      border-radius: 0 0 .5rem 0;
    .ad-log
      position: relative
      width: .7rem
      height: .7rem
      left: .65rem
      top: .15rem
      display: inline-block
      background: url(//imgs.qunarzz.com/piao/fusion/1606/44/2605d5bd522e109a.png)
      background-size: .7rem .7rem
      border-radius: .1rem
    .ad-txt
      display: inline-block
      position: relative
      top: .08rem
      left: .8rem
      line-height: .32rem
      font-size: .24rem
      color: #fff
    .ad-link
      position: absolute
      top: .22rem
      right: .2rem
      width: 1.4rem
      height: .56rem
      line-height: .56rem
      text-align: center
      border: .02rem solid #1d8f96
      border-radius: .08rem
      font-size: .26rem
      color: #1d8f96
</style>
