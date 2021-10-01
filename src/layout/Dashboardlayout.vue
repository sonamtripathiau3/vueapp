<template>
  <div class="container">
    <div class="row" v-if="message=='navbar'">
      {{message}}
      <Navbar />
    </div>
    <div class="row" v-else>
      <h6>{{message}}</h6> 
      <Footer/>
    </div>
    </div>
</template>
<style lang="scss">
</style>
<script>
import Navbar from "./navbar.vue";
import Footer from "./footer.vue";

export default {
  name:"Dashboard",
  components: {
      Navbar,
      Footer
  },
  props:[
    'message'
  ]
};
</script>
