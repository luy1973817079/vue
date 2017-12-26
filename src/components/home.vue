<template>
  <div id="home">
  <h1>{{title1}}</h1>
  <app-header v-on:titleChanged="updateTitle($event)"v-bind:title="title"></app-header>
  <users v-bind:users="users"></users>
  <users v-bind:users="users"></users>
  <app-footer  v-bind:title="title"></app-footer>

  </div>
</template>

<script>
import Header from './Header'
import Users from './Users'
import Footer from './Footer'


export default {
  name: 'home',
  data(){
   return{
   title1:'这是第一个Vue脚手架项目',
    title:'传递的值是一个string number boolean',
    users: [

          ]
   }
  },methods:{
    updateTitle :function(title){
      this.title = title
    }
  },
  components: {
    "app-header":Header,
    "users":Users,
    "app-footer":Footer
  },
  created(){
    this.$http.get("http://jsonplaceholder.typicode.com/users")
               .then((data)=>{
                  this.users = data.body
        })
  }
}
</script>

<style>

</style>
