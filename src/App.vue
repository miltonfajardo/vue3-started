<template>
  <h1>Vue JS</h1>
  <!-- <CarOptions />
  <hr />
  <CarComposition /> -->
  <Car :power="power" :upPower="upPower" @downPower="downPower" />
</template>

<script>
/* import CarComposition from "./components/CarComposition";
import CarOptions from "./components/CarOptions"; */
import { ref } from "vue";
import Car from "./components/Car";
export default {
  components: {
    /* CarComposition,
    CarOptions, */
    Car,
  },
  setup() {
    let power = ref(38);

    const upPower = () => {
      power.value++;
    };

    const downPower = () => {
      power.value--;
    };

    return {
      power,
      upPower,
      downPower,
    };
  },
};
</script>

<style></style>
