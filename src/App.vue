<template>
  <h1>Dynamic Component Sample</h1>
  <HelloWorld :component-names="componentNames1"/>
  <h3>↓ 別の配列を渡す</h3>
  <HelloWorld :component-names="componentNames2"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data: function () {
    return {
      componentNames1: [
        'HelloOne',
        'HelloTwo',
        'HelloThree',
      ],
      componentNames2: [
        'TestOne',
        'TestTwo',
        'TestThree',
      ]
    }
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

h3 {
  margin-top: 50px;
  margin-bottom: 15px;
}
</style>
