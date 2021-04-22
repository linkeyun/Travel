<template>
  <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/68/de862f94e383a6.jpg_r_640x214_f9df927b.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/f6/82acfa5c7f472c.jpg_r_640x214_508da3cb.jpg'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/fc/c9ac09bb08e382.jpg_r_640x214_6b9eb488.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff
.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 37%
  .swiper-img
    width: 100%
</style>
