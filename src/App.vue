<template>
  <div id="app">
    <div class="p-4 text-gray-900">
      <section v-for="className in classNames" :key="className">
        <ui-section-header>
          {{ className }}
        </ui-section-header>
        <div :class="className">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut quam
          felis, aliquet et tincidunt nec, cursus eget tellus. Mauris quis nisl
          tristique augue vehicula mattis. Nam elementum maximus augue nec
          commodo. Nulla vehicula tortor at nisl sodales, ac iaculis erat
          facilisis. Suspendisse pulvinar aliquet turpis a varius. Vestibulum
          eget commodo libero, nec accumsan sem. In pretium nisl in leo commodo
          egestas. Praesent bibendum nisi massa, non ullamcorper tellus
          malesuada at.
        </div>
      </section>
    </div>
    <div class="p-4">
      <ui-section-header>
        ui-button
      </ui-section-header>
      <ui-button tag="a">Login</ui-button>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import UiButton from "./components/UiButton.vue";
import UiSectionHeader from "./components/UiSectionHeader.vue";

export default Vue.extend({
  name: "app",
  components: { UiButton, UiSectionHeader },
  data() {
    return {
      classNames: [
        "heading-medium",
        "heading-large",
        "caption",
        "text-tiny",
        "text-small",
        "text-medium",
        "text-large"
      ]
    };
  }
});
</script>
