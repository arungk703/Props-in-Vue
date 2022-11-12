<template>
  <h1>Hii, I am {{ name }}</h1>
  <h2>My Skills are:</h2>
  <h3
    :class="changedClass"
    @mouseover="isChanged"
    v-for="(skill, index) in skills"
    :key="index"
  >
    {{ skill }}
  </h3>
</template>


<script>
export default {
  name: "child-component",
  props: ["name", "skills"],
  data() {
    return {
      changedClass: "normal",
    };
  },
  methods: {
    isChanged() {
      this.changedClass = "promoted";
    },
  },
};
</script>

<style scoped>
.promoted {
  background-color: aquamarine;
}
.normal {
  color: blue;
}
</style>