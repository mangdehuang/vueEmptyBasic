<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
var html = document.documentElement;
var width = html.getBoundingClientRect().widht;
html.style.fontSize = width / 15 + "px";
export default {
  name: "App"
};
</script>

<style lang='scss'>
@import "assets/icon/iconfont.css";
@import "assets/style/global.scss";
</style>
