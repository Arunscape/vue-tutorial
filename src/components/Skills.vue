<template>
  <div class="hello">
    <div class="holder"></div>
    <ul>
      <li v-for="(data, index) in skills" :key="index">
        {{ index }}. {{ data.skill }}
      </li>
    </ul>

    <p v-if="skills.length >= 1">You have 1 or more skills</p>
    <p v-else>Really???</p>
  </div>
</template>

<script>
export default {
  name: "Skills",
  data() {
    return {
      skills: [{ skill: "vuejs" }, { skill: "front end dev" }]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
