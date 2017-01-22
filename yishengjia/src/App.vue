<template>
  <div id="app">
    <img src="./assets/wholelife-banner.jpg" >
    <img src="./assets/wholelife.jpg" v-if="portable > 1000">
    <img src="./assets/wholelife-portable.jpg" v-if="portable <= 1000">
  </div>
</template>

<script>


export default {
  name: 'app',
  data() {
    return {
      portable: document.body.clientWidth
    }
  },
  components: {

  },
  watch: {
    portable: function() {
      return document.body.clientWidth
    }
  }
}
</script>

<style lang="less">
*{
  margin: 0;
  padding: 0;
}
#app {
  width: 100%;
  img {
    width: 100%;
  }
}
</style>
