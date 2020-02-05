<template>
  <component
    :is="tag"
    class="cursor-pointer inline-block py-2 px-4 text-white bg-blue-900 leading-normal"
  >
    <slot>Login with dpa ID</slot>
  </component>
</template>

<script lang="ts">
import Vue, { PropType } from "vue";

export default Vue.extend({
  props: {
    tag: {
      type: String,
      default: "button",
      validator(val) {
        return ["button", "input", "a"].includes(val);
      }
    }
  }
});
</script>

<style>
</style>
