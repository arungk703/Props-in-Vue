<template>
  <Child :name="name" :skills="skills"> </Child>
</template>

<script>
import Child from "./components/Child.vue";
export default {
  name: "App",
  components: {
    Child,
  },
  data() {
    return {
      name: "Arun",
      skills: ["Java", "Python", "HTML", "CSS", "JS", "Vue.js", "Git"],
    };
  },
};
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
