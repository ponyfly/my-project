<template>
  <div>
    <h1>{{count}}</h1>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
  </div>
</template>

<script>
  import store from '../../store/store'

  export default {
    data() {
      return {}
    },
    computed: {
      count() {
        return store.state.counter
      }
    },
    methods: {
      increment () {
        store.commit('increment')
      },
      decrement () {
        store.commit('decrement')
      }
    }
  }
</script>

<style>

</style>