<template>
  <Mug>
    <Cold v-if="isIced" />
    <Hot v-else />
    <Contents>
      <template v-slot:top>
        <Creamer :selectedCreamer="props.selectedCreamer" />
      </template>
      <template v-slot:mid>
        <Syrup :selectedSyrup="props.selectedSyrup" />
      </template>
      <template v-slot:bottom>
        <Base :selectedBase="props.selectedBase" />
      </template>
    </Contents>
  </Mug>
</template>
<script setup lang="ts">
import Base from "./Base.vue";
import Cold from "./Cold.vue";
import Contents from "./Contents.vue";
import Creamer from "./Creamer.vue";
import Hot from "./Hot.vue";
import Mug from "./Mug.vue";
import Syrup from "./Syrup.vue";

import type {
  BaseBeverageType,
  CreamerType,
  SyrupType
} from "../stores/beverage";

type Props = {
  isIced: boolean;
  selectedBase: BaseBeverageType;
  selectedCreamer: CreamerType;
  selectedSyrup: SyrupType;
};

const props = defineProps<Props>();
</script>
