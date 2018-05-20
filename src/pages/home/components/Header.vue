<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe6aa;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
// scoped不对其他组件样式有影响，引用stylus来写css样式,
// reset.css 中HTML的font-size为50px，1rem = html font-size = 50px,此处高度为43px
// 在样式表中引用另一个样式表时需要在路径前面加~
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      // 使用line-height来居中文字，且与高度值相同
      line-height: .64rem
      background: #fff
      border-radius: .1rem
      padding-left: .2rem
      margin-left: .2rem
      margin-top: .12rem
      color: #ccc
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      .arrow-icon
        font-size: .24rem
</style>
