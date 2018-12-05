<template>
  <div class="Header"></div>
</template>
<script>
export default {
  name: "Header",
  data() {
    return {
      dataList: []
    };
  },
  created() {
    this.$axios.get("api/news/latest").then(data => {
      this.dataList = data.data;
      console.log(this.dataList);
    });
  }
};
</script>
<style lang="scss" scoped>
@import "@/assets/style/global.scss";
</style>
    