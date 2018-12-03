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
    this.$axios
      .get(
        "/api/v1.5/tr.json/translate?key=trnsl.1.1.20181029T090347Z.f10d529bb9b867e0.802ade551d8acf71e854d2af44bd0153a58bf181&text=测试&lang=en"
      )
      .then(data => {
        this.dataList = data.data;
        console.log(this.dataList);
      });
  }
};
</script>
<style lang="scss" scoped>
@import "@/assets/style/global.scss";
</style>
    