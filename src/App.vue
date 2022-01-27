<template>
  <Navbar></Navbar>
  <Header></Header>
  <Calendar></Calendar>
  <!--<img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>-->
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Navbar from "./components/structure/Navbar";
import Header from "./components/structure/Header";
import Calendar from "./components/Calendar";


export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    Calendar
  }
}
</script>

<style>

</style>
