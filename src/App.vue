<!-- html 요소 -->
<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/> -->

  <h1>count: {{ count }}</h1>
  <button @click="countUp">countUp!!!</button>

  <h1>todo title: {{ todo.title }}</h1>
  <h1>todo isDone: {{ todo.isDone }}</h1>
  <button @click="makeTodoToggle">makeTodoToggle!!!</button>

  <ul id="array-rendering">
    <li v-for="item in myArray" v-bind:key="item">
      {{ item }}
    </li>
  </ul>

  <button @click="addItemToArray">아이템추가</button>
  <button @click="removeItemFromArray">아이템삭제</button>

</template>

<!-- 스크립트 - 로직 && 데이터 변수   -->
<script>
// 콤포넌트를 임포트로 가져온다 
// import HelloWorld from './components/HelloWorld.vue'

import { ref, reactive } from 'vue'

export default {
  // 해당 콤포넌트의 이름이 App 입니다 
  name: 'App',
  //
  components: {
    // HelloWorld // 핼로우 월드 콤포넌트를 사용 할께요 
  },

  setup() {
    
      const count = ref(0)

      const todo = reactive({ title: '빨래하기', isDone: false })

      const myArray = reactive([])

      const countUp = () => {
        count.value++
        console.log('countUp() called', count.value);
      };

      const makeTodoToggle = () => {
        todo.isDone = !todo.isDone
        console.log('makeTodoToggle() called', todo.isDone);
      };

      const addItemToArray = () => {
        myArray.push('🔥');
        console.log('addItemToArray() called', myArray.count);
      };

      const removeItemFromArray = () => {
        myArray.pop();
        console.log('addItemToArray() called', myArray.count);
      };

      // expose to template
      return {
        count,
        todo,
        countUp,
        makeTodoToggle,
        myArray,
        addItemToArray,
        removeItemFromArray
      }
  }
}
</script>

<!-- 스타일링  -->
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
