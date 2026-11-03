<template>
   <div
    class="syrup"
    :style="{ '--syrup-color': props.selectedSyrup.color }"
  ></div>
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
  background-image: repeating-linear-gradient(
    45deg,
    var(--syrup-color) 0px,
    var(--syrup-color) 10px,
    #E1CF95 10px,
    #E1CF95 20px
);
  position: relative;
  width: 100%;
  height: 20%;
  animation: pour-tea 2s 1s forwards;
  z-index: 2;
}
</style>
