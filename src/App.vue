<template>
  <div>
    <app-header></app-header>
    <app-contacts></app-contacts>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from'./components/Header.vue';
import Footer from './components/Footer.vue';
import Contacts from './components/Contacts.vue';

export default {
  components:{
    'app-header': Header,
    'app-footer': Footer,
    'app-contacts': Contacts
  },
  data () {
    return {

    }
  }
}
</script>

<style scoped>

</style>
