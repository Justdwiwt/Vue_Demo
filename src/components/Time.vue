<template>
  <div id="app">
    {{ date }}
  </div>
</template>

<script>
// export default {
//   name: 'Time'
// }
import Vue from 'vue'
var app = new Vue({
  el: '#app',
  data: {
    date: new Date()
  },
  mounted: function () {
    var _this = this
    this.timer = setInterval(function () {
      _this.data = new Date()
    }, 1000)
  },
  beforeDestroy: function () {
    if (this.timer) {
      clearInterval(this.timer)
    }
  }
})
</script>

<style scoped>
</style>
