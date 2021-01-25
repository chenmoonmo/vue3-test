<template>
  <button @click="changeMsg">changeMsg</button>
  <h1 class="hello">{{message}}</h1>
</template>

<script>
import { toRefs, ref } from 'vue'
export default {
  props: {
    name: String
  },
  setup(props, context) {
    const { name } = toRefs(props)
    let message = ref(`hello ${name.value}!`)
    const changeMsg = () => {
      return (message.value = 'hello world')
    }
    return { message, changeMsg }
  }
}
</script>

<style>
</style>