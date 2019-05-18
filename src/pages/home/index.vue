<template>
  <div>
    <!--搜索部分 -->
    <div class="searchBox">
      <div class="search">
        <icon type="search" size="20"></icon>
        <span>搜索</span>
      </div>
    </div>
    <!-- 轮播图部分 -->
    <swiper :indicator-dots="indicatorDots">
      <swiper-item v-for="(item,index) in imgUrls" :key="index">
        <image :src="item" class="slide-image" width="355" height="150"></image>
      </swiper-item>
    </swiper>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgUrls: [
        "https://images.unsplash.com/photo-1551334787-21e6bd3ab135?w=640",
        "https://images.unsplash.com/photo-1551214012-84f95e060dee?w=640",
        "https://images.unsplash.com/photo-1551446591-142875a901a1?w=640"
      ],
      indicatorDots: true
    };
  }
};
</script>

<style lang="css" scoped>
.searchBox {
  padding: 10px;
  height: 30px;

  background-color: #e8424d;
}
.searchBox .search {
  background-color: #fff;
  text-align: center;
}
.searchBox .search icon {
  vertical-align: middle;
  margin-right: 5px;
}
</style>
