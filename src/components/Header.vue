<template>
  <header v-on:click="changeTitle">
    <h1>{{title1}}{{title}}</h1>
  </header>
</template>

<script>
export default {
  name: 'app-header',
  props:{
    title:{
      type:String
    }
  },
  data () {
    return {
      title1: 'Vue.js demo '
    }
  },
  methods:{
    changeTitle:function(){
      this.$emit("titleChanged","子组件向父组件传值")
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1{background: green;color: red;padding:10px;text-align:center;}
</style>
