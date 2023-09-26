<template>
  <!-- <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num < 0">The number is Negative</h2>
  <h2 v-else>The number is not zero</h2> -->
  <div>
    <h1 v-for="name in names" :key="name">{{ name }}</h1>
    <h1 v-for="name in fullName" :key="name">{{ name.first }} {{name.last}}</h1>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["bruce", "clark", "diana"],
      fullName: [
        {first:'Bruce', last:'Wayne'},
        {first:'Clark', last:'Kent'},
        {first:'Princess', last:'Diana'},
      ]
    };
  },
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
