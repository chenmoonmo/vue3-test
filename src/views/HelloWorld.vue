<template>
  <h1 class="hello">{{message}}</h1>
</template>

<script>
import { toRef, ref } from 'vue'
export default {
  props: {
    name: String
  },
  setup(props) {
    const { name } = toRef(props)
    console.log(props.name)
    const message = `hello ${props.name}!`
    return { message }
  }
}
</script>

<style>
</style>