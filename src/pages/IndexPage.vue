<template>
  <q-page class="flex flex-center">
    <div
      id="canvas"
      @click="changeColor"
      :style="`background-color: ${COLORS[colorIndex]};`"
    ></div>
  </q-page>
</template>

<script setup>
import { ref } from "vue";

const COLORS = [
  "#ff0000",
  "#00ff00",
  "#0000ff",
  "#ffff00",
  "#00ffff",
  "#ff00ff",
  "#ffffff",
  "#CCCCCC",
  "#888888",
  "#444444",
  "#000000",
];
var colorIndex = ref(0);
function changeColor() {
  colorIndex.value = (colorIndex.value + 1) % COLORS.length;
}

defineOptions({
  name: "IndexPage",
});
</script>

<style scoped>
#canvas {
  width: 100%;
  height: 100vh;
}
</style>
