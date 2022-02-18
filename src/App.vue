<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{title}}</h1>
    <Child_parent v-on:changeTitle="updateTitle($event)" />
  </div>
</template>
<script>
import Child_parent from './components/Child_parent.vue'
export default {
  name: 'App',
  components: {
    Child_parent
  },
 data() {
   return {
     title:'Bilal Khan'
   }
 },
  methods:{
    updateTitle(title)
    {
      this.title=title
    }
  }
};
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
