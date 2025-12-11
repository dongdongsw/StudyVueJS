<template>
  <HeaderCont/>
  <router-view/>
  <!-- router/index.js에서 어떤 화면을 보여줄지 결정 -->
</template>

<script>
import HeaderCont from './components/HeaderCont.vue'

export default {
  name: 'App',
  components: {
    HeaderCont
  }
}
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
