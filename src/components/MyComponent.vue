<!-- html 요소 -->
<template>
    <h1>타이틀: {{ title }} 입니다.</h1>
    <h1>count: {{ count }}</h1>
    <button @click="sayHello">인사하세요~</button>
    <button @click="countUp">카운트 업</button>
</template>

<!-- 스크립트 - 로직 && 데이터 변수   -->
<script>
export default {
    name: 'MyComponent',
    // 사용하는 데이터 변수 
    data(){
        return {
            title: '쩡대리',
            count: 0
        }
    },
    // 사용하는 메소드 들 정의 
    methods: {
        sayHello(){
            this.title = "안녕하세요?";
        },
        countUp(){
            this.count += 1;
        }
    }
}
</script>

<!-- 스타일링  -->
<style scoped>
    h1 {
        background: green;
        color: white;
    }
</style>