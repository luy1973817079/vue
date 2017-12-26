<template>
  <footer>
    <p>{{copy}}{{title}}</p>
  </footer>
</template>

<script>
export default {
  name: 'app-footer',
  props:{
      title:{
        type:String
      }
  },
  data () {
    return {
      copy:"copy @right 2017"
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  p{background:black;color:#fff;padding:5px;text-align:center;}
</style>
