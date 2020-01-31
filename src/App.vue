<template>
  <div id="app">
    <HelloWorld />
    <!-- <Concide/>
    <Children :data="item"/> -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// import Concide from './components/Concide'
// import Children from './components/Children'

export default {
  name: 'app',
  components: {
    HelloWorld,
    // Concide,
    // Children
  },
  data() {
    return {
      item:"12345"
    }
  },
}
</script>

<style lang="less">

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  // background-color: #333;  
//   position: relative;
// top: 40px;
  width: 100%;
  height: 100%;
  margin: 0;
}
</style>
