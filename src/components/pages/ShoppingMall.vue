<template>
  <div>
    <div class="search-bar">
      <van-row>
        <van-col span="3"><img :src="logoIcon" alt="" width="100%" class="logo-icon"></van-col>
        <van-col span="16"><input type="text" class="search-input"></van-col>
        <van-col span="5"><van-button size="mini">查找</van-button></van-col>
      </van-row>
    </div>
    <div class="swiper-area">
      <van-swipe :autoplay="1000">
        <van-swipe-item v-for="(banner, index) in bannerPicArray" :key="index">
          <img v-lazy="banner.imageUrl" alt="" width="100%" />
        </van-swipe-item>
      </van-swipe>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'Shopping Mall',
      logoIcon: require('../../assets/images/logo.png'),
      bannerPicArray:[
        {imageUrl:'http://7xjyw1.com1.z0.glb.clouddn.com/simleVueDemoPic001.jpg'},
        {imageUrl:'http://7xjyw1.com1.z0.glb.clouddn.com/simleVueDemoPic002.jpg'},
        {imageUrl:'http://7xjyw1.com1.z0.glb.clouddn.com/simleVueDemoPic003.jpg'},
      ]
    }
  }
}
</script>

<style scoped>
.search-bar{
  height: 2.2rem;
  background-color: #e5017d;
  line-height: 2.2rem;
}
.search-input{
  width: 100%;
  height: 1.3rem;
  border: none;
  border-bottom: 1px solid 1px !important;
  background-color: #e5017d;
  color: #fff;
}
.logo-icon{
  padding-top: .2rem;
  padding-left: .3rem;
}
.swiper-area{
  width: 20rem;
  clear: both
}
</style>
