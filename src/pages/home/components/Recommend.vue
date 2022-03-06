<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script type="text/javascript">
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1511/d2/d2aec2dfc5aa771290.water.jpg_200x200_69e4a80d.jpg',
        title: '南山滑雪场',
        desc: '美丽的南山滑雪场，非常好玩'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1511/d2/d2aec2dfc5aa771290.water.jpg_200x200_69e4a80d.jpg',
        title: '南山滑雪场',
        desc: '美丽的南山滑雪场，非常好玩'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1511/d2/d2aec2dfc5aa771290.water.jpg_200x200_69e4a80d.jpg',
        title: '南山滑雪场',
        desc: '美丽的南山滑雪场，非常好玩'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    margin-top: .2rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .4rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
