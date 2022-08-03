<template>
  <div>{{ msg }}</div>
  <input type="text" />
  <button @click="handleClick">点击</button>
</template>

<script>
import { defineComponent, ref } from "vue";

import { modification } from "./assets/js/index";

export default defineComponent({
  name: "App",
  setup() {
    const msg = ref("hello world");

    function handleClick() {
      msg.value = modification(msg.value);
    }

    return {
      msg,
      handleClick,
    };
  },
});
</script>

<style>
</style>