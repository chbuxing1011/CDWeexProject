<template>
  <div class="wrapper" @click="update">
    <image :src="logoUrl" class="logo"></image>
    <text class="title">Hello {{target}}</text>
  </div>
</template>

<style>
  .wrapper { align-items: center; margin-top: 120px; }
  .title { font-size: 48px; }
  .logo { width: 360px; height: 82px; }
</style>

<script>
  require('./a.vue');
  require('./group/indicator.vue');
  require('./group/list.vue');
  require('./group/input.vue');
  require('./group/scroller.vue');
  require('./module/navigator.vue');
  require('./module/stream.vue');
  const navigator = require('@weex-module/navigator');
//  const storage = require('@weex-module/storage');

  export default {
    data: {
      logoUrl: 'https://alibaba.github.io/weex/img/weex_logo_blue@3x.png',
      target: 'World'
    },
    methods: {
      update: function (e) {
        this.target = 'Weex111'
        console.log('target:', this.target)
      }
    }
  }
</script>
