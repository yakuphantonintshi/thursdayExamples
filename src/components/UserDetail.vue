<template>
  <div>
    <h2>User Detail</h2>
    <p>{{ firstName }} {{ lastName }}</p>
    <h2>Age</h2>
    <p>{{ age }}</p>
    <h2>Gender</h2>
    <p>{{ gender }}</p>
  </div>
</template>

<script>
export default {
  name: 'UserDetail',
  props:["firstName", "lastName", "age", "gender"]
}
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



