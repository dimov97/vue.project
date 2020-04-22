<template>
  <div id="app">
    <div v-for="(text, i) in tips" :key="i">
      <tip :text-for-tip="text"/>
      <button @click="showNumber(i)"> show {{ i }}</button>
    </div>
  </div>
</template>

<script>
import Tip from '@/components/ui/Tip.vue'

export default {
  name: 'App',
  components: {
    Tip,
  },
  data() {
    return {
      tips: ['1', '2', '3', 4, 5],
    }
  },
  methods: {
    showNumber(val) {
      console.log(val);
    }
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-color: red;
  > div {
  }
}
</style>
