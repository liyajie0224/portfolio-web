<template>
  <div class="block">
    <!-- <span class="demonstration">作品集demo</span> -->
    <el-carousel indicator-position="outside" :height="bannerHeight + 'px'"  :autoplay="false" :loop="true">
      <el-carousel-item v-for="(item,index) in BannerImg" :key="index">
        <img src="../assets/portfolio web/WEB.png" v-if="index == 0" class="bannerImg" />
        <img src="../assets/portfolio web/WEB2.png" v-if="index == 1" class="bannerImg" />
        <img src="../assets/portfolio web/WEB3.png" v-if="index == 2" class="bannerImg" />
        <img src="../assets/portfolio web/WEB4.png" v-if="index == 3" class="bannerImg" />
        <img src="../assets/portfolio web/WEB5.png" v-if="index == 4" class="bannerImg" />
        <img src="../assets/portfolio web/WEB6.png" v-if="index == 5" class="bannerImg" />
        <img src="../assets/portfolio web/WEB7.png" v-if="index == 6" class="bannerImg" />
        <img src="../assets/portfolio web/WEB8.png" v-if="index == 7" class="bannerImg" />
        <img src="../assets/portfolio web/WEB9.png" v-if="index == 8" class="bannerImg" />
        <img src="../assets/portfolio web/WEB10.png" v-if="index == 9" class="bannerImg" />
        <img src="../assets/portfolio web/WEB11.png" v-if="index == 10" class="bannerImg" />
        <img src="../assets/portfolio web/WEB12.png" v-if="index == 11" class="bannerImg" />
        <img src="../assets/portfolio web/WEB13.png" v-if="index == 12" class="bannerImg" />
        <img src="../assets/portfolio web/WEB14.png" v-if="index == 13" class="bannerImg" />
        <img src="../assets/portfolio web/WEB15.png" v-if="index == 14" class="bannerImg" />
      </el-carousel-item>
    </el-carousel>
  </div>
</template>
<script>
export default {
  data() {
    return {
      BannerImg: [
        { url: require("../assets/portfolio web/WEB.png") },
        { url: require("../assets/portfolio web/WEB2.png") },
        { url: require("../assets/portfolio web/WEB3.png") },
        { url: require("../assets/portfolio web/WEB4.png") },
        { url: require("../assets/portfolio web/WEB5.png") },
        { url: require("../assets/portfolio web/WEB6.png") },
        { url: require("../assets/portfolio web/WEB7.png") },
        { url: require("../assets/portfolio web/WEB8.png") },
        { url: require("../assets/portfolio web/WEB9.png") },
        { url: require("../assets/portfolio web/WEB10.png") },
        { url: require("../assets/portfolio web/WEB11.png") },
        { url: require("../assets/portfolio web/WEB12.png") },
        { url: require("../assets/portfolio web/WEB13.png") },
        { url: require("../assets/portfolio web/WEB14.png") },
        { url: require("../assets/portfolio web/WEB15.png") }
      ],
      bannerHeight:Number
    };
  },
  mounted() {
    this.setSize();
    const that = this;
    window.addEventListener(
      "resize",
      function() {
        that.screenWidth = $(window).width();
        that.setSize();
      },
      false
    );
  },
  methods: {
    setSize: function() {
      // this.bannerHeight = (740 / 2560) * this.screenWidth;
      // if (this.bannerHeight > 740) this.bannerHeight = 740;
      // if (this.bannerHeight < 360) this.bannerHeight = 360;
      this.bannerHeight = document.body.clientWidth / 3
    }
  }
};
</script>
<style>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
.bannerImg {
  width: 100%;
  height: inherit;
  min-height: 360px;
  min-width: 1400px;
}
.block,.el-carousel,.el-carousel__container {
  width: 100%;
      height: 100%;
      margin: 0;
}

</style>