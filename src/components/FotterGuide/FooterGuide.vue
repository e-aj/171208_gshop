<template>
  <div class="footer_guide">
    <span class="guide_item" :class="{on:'/msite' === $route.path}" @click="goTo('/msite')">
      <span class="tiem">
        <i class="iconfont icon-waimai-"></i>
      </span>
      <span>外卖</span>
    </span>
    <span  class="guide_item " :class="{on:'/search' === $route.path}" @click="goTo('/search')">
      <span class="tiem_icon">
        <i class="iconfont icon-search"></i>
      </span>
      <span>搜索</span>
    </span>
    <span class="guide_item " :class="{on:'/order' === $route.path}" @click="goTo('/order')">
      <span class="tiem_icon">
        <i class="iconfont icon-weibiaoti-"></i>
      </span>
      <span>订单</span>
    </span>
    <span  class="guide_item " :class="{on:'/profile' === $route.path}" @click="goTo('/profile')">
      <span class="tiem_icon">
        <i class="iconfont icon-icon"></i>
      </span>
      <span>我的</span>
    </span>

  </div>
</template>

<script>
  export default {
    methods: {
      goTo (path) {
        this.$router.replace(path)
      }
    }
  }
</script>

<style scoped>
  .footer_guide{
    border-top: 1px solid #e4e4e4;
    position: fixed;
    z-index: 100;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #fff;
    width: 100%;
    height: 50px;
    display: flex;
  }
  .guide_item {
      display: flex;
      flex: 1;
      text-align: center;
      flex-direction: column;
      align-items: center;
      margin: 5px;
      color: #999;
    }
  .on{
        color: #02a774;
      }
  span{
    font-size: 12px;
    margin-top: 2px;
    margin-bottom: 2px;
  }
  .iconfont{
    font-size: 22px;
  }
</style>
