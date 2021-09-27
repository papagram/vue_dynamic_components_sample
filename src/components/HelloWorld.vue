<template>
  <component v-for="componentName in componentNames" :is="componentName" :key="componentName" />
</template>

<script>
import { defineAsyncComponent } from 'vue'

const HelloOne = defineAsyncComponent(() => import('./HelloOne.vue'))
const HelloTwo = defineAsyncComponent(() => import('./HelloTwo.vue'))
const HelloThree = defineAsyncComponent(() => import('./HelloThree.vue'))
const TestOne = defineAsyncComponent(() => import('./TestOne.vue'))
const TestTwo = defineAsyncComponent(() => import('./TestTwo.vue'))
const TestThree = defineAsyncComponent(() => import('./TestThree.vue'))

export default {
  name: 'HelloWorld',
  components: {
    HelloOne,
    HelloTwo,
    HelloThree,
    TestOne,
    TestTwo,
    TestThree
  },
  props: {
    componentNames: Array
  }
}
</script>
