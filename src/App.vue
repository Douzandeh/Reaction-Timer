<template>
 <h1>OpenCode Reaction Timer </h1>
 <button @click="start" :disabled="isPlaying">Playe</button>
 <Block v-if="isPlaying" :delay="delay"/>
</template>

<script>
import Block from "./components/Block.vue"
export default {
  name: 'App',
  components: {Block},
  data(){
    return{
      delay: null,
      isPlaying: false
    }
  },
  methods:{
    start(){
      this.delay = 2000 + Math.random() * 5000
      this.isPlaying = true
      console.log(this.delay);
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
  color: #444;
  margin-top: 60px;
}
</style>