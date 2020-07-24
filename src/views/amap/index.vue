<template>
  <div class="amap-wrap">
    <el-amap vid="amapContainer"> </el-amap>
  </div>
</template>

<script>
import { AMapManager, lazyAMapApiLoaderInstance } from 'vue-amap';
export default {
  name: 'amap',
  data() {
    return {
      map: null,
      zoom: 12,
    };
  },
  mounted() {
    lazyAMapApiLoaderInstance.load().then(() => {
      // your code ...
      this.map = new AMap.Map('amapContainer', {
        center: [116.404765, 39.918052],
        zoom: this.zoom,
      });
    });
  },
};
</script>

<style lang="scss" scoped>
.amap-wrap {
  height: 100vh;
}
</style>
