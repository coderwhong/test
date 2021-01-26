<template>
  <div class="hello">
    <h3>我是父组件</h3>
    <p>{{star}}</p>
    <child :title.sync="star"></child>
  </div>
</template>

<script>
  import child from "./child.vue"
  export default {
    data() {
      return {
        star: '华为'
      }
    },
    components: {
      child,
    }
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
