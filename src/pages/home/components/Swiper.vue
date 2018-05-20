<template>
    <div class="wrapper">
      <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"  />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
export default{
  name: 'HomeSwiper',
  data () {
    return {
      notNextTick: true,
      swiperOption: {
        // 未显示出来小圆点
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/d5/fb4a5c81cd87a002.jpg_890x330_901edbfc.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/de/47d98076af29f202.jpg_750x200_7888b7c9.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
// 改变小圆点的样式
    .wrapper >>> .swiper-pagination-bullet-active
      background: red
     .wrapper
      overflow: hidden
      width: 100%
      height: 0
      padding-bottom: 31.25%
      background #eee
    .swiper-img
      width:100%
</style>
