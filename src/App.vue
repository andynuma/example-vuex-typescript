<template>
  <div id="app">
    <Counter />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Counter from "./components/Counter.vue";
import { employeeModule } from "./store/modules/employee";

@Component({
  components: {
    Counter
  }
})
export default class App extends Vue {
  mounted() {
    employeeModule.setEmployee();
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
