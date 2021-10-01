<template>
<h1> Type navbar/ users to view them</h1>
  <input v-model="message">
   <div  class="mt-5" v-if="message=='users'">
  <Users/>
</div>
<div class="mt-5" v-else>
  <Dashboard v-bind:message="message"/>
</div>

</template>

<script>
import Users from "./components/users.vue"
import Dashboard from "./layout/Dashboardlayout.vue"

export default {
  name: 'App',
  components: {
    Users,
    Dashboard
  },
  data () {
    return {
      message: "hello"
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
  color: #2c3e50;
  margin-top: 60px;
}
</style>
