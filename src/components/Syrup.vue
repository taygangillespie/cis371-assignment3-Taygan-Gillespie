<template>
  <div class="syrup" :style="{ backgroundColor: props.selectedSyrup.color }"></div>
</template>

<script setup lang="ts">
import type { SyrupType } from "../stores/beverage";
type SyrupProp = {
  selectedSyrup: SyrupType;
};
const props = defineProps<SyrupProp>();

</script>
<style lang="scss" scoped>
.syrup {
  transform: translateY(400%);
  position: relative;
  width: 100%;
  height: 20%;
  animation: pour-tea 2s 1s forwards;
  z-index: 2;
}
</style>
