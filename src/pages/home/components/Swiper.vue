<template>
    <div class="wrapper">
      <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"  />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
export default{
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      notNextTick: true,
      swiperOption: {
        // 未显示出来小圆点
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  // 定义轮播图显示在第一页上
  computed: {
    showSwiper () {
      return this.list.length
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
