<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
export default {
  name: "App",
  created() {
    // const api = `${process.env.APIPATH}/api/${process.env.CUSTOMPATH}/products`;
    const api = "https://vue-course-api.hexschool.io/api/lpstony/products/all";
    console.log(process.env.APIPATH, process.env.CUSTOMPATH);
    this.$http.get(api).then(response => {
      console.log("RESPONSE DATA", response.data);
    });
  }
};
</script>

<style lang='scss'>
@import "./assets/all";
</style>