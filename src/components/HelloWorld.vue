<script setup>
import { onMounted, ref } from "vue";
import MapCanvas from "./c.ts";

const cf = ref();
onMounted(() => {
  new MapCanvas(cf.value);
});
</script>

<template>
  <button>开始签名</button>
  <button>完成</button>
  <canvas ref="cf" class="my-canvas"></canvas>
</template>

<style scoped>
.my-canvas {
  height: 100vh;
}
</style>
