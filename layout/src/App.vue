<template>
  <div id="app">
    <component v-bind:is="layout"/>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class App extends Vue {
  private defaultLayout: string = 'default';

  get layout(): string {
    return (this.$route.meta.layout || this.defaultLayout) + '-layout';
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
