<template>
  <component v-for="componentName in componentNames" :is="componentName" :key="componentName" />
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    componentNames: Array
  }
}
</script>
