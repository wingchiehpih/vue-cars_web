<template>
  <div class="amap-wrap">
    <Map />
  </div>
</template>

<script>
import Map from '../amap/index';
export default {
  name: 'index',
  components: {
    Map,
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.amap-wrap {
  height: 100vh;
}
</style>
