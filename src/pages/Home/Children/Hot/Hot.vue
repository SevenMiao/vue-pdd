<template>
  <div class="hot">
    <!-- 轮播图 -->
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <img src="./../../imgs/hot_ad/pic_1.png" alt width="100%" />
        </div>
        <div class="swiper-slide">
          <img src="./../../imgs/hot_ad/pic_2.png" alt width="100%" />
        </div>
        <div class="swiper-slide">
          <img src="./../../imgs/hot_ad/pic_3.png" alt width="100%" />
        </div>
        <div class="swiper-slide">
          <img src="./../../imgs/hot_ad/pic_4.png" alt width="100%" />
        </div>
      </div>
      <!-- 如果需要分页器 -->
      <div class="swiper-pagination"></div>
    </div>
      <hot-nav/>
      <hot-shop-list/>
  </div>
</template>
<script>
import Swiper from "swiper";
import HotNav from "./HotNav";
import HotShopList from "./HotShopList";
import "swiper/dist/css/swiper.min.css";

export default {
  name: "Hot",
  components:{
    HotNav,
    HotShopList
  },
  data: function() {
    return {};
  },
  mounted() {
    new Swiper(".swiper-container", {
      autoplay: true, // 自动播放
      loop: true, // 循环模式
      // 如果需要分页器
      pagination: {
        el: ".swiper-pagination"
      }
    });
  }
};
</script>
<style scoped lang="stylus" ref="stylesheet/stylus">
.hot
  width 100%
  height 100%
  padding-top 67.2px
  background-color #f5f5f5
</style>