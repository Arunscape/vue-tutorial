<template>
  <div class="hello">
    <div class="holder"></div>
    <ul>
      <li v-for="(data, index) in skills" :key="index">
        {{ index }}. {{ data.skill }}
      </li>
    </ul>

    <div v-bind:class="alertObject"></div>
  </div>
</template>

<script>
export default {
  name: "Skills",
  data() {
    return {
      skills: [{ skill: "vuejs" }, { skill: "front end dev" }],
      alertObject: {
        alert: true
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.alert {
  background-color: yellow;
  width: 100%;
  height: 30px;
}
.another-class {
  border: 5px solid black;
}
</style>
