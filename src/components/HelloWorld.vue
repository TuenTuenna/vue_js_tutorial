<template>
  <div class="hello">

    <my-component></my-component>

    <h1>{{ msg }}</h1>
    <h1>HelloWorld 콤포넌트 입니다</h1>
  </div>
</template>

<script>

import MyComponent from './MyComponent.vue'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    MyComponent
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
