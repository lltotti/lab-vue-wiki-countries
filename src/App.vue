<template>
  <div class="app">
    <Navbar/>
    <CountriesList/>
    <router-view/>

    
  </div>
</template>



<script setup>
import Navbar from "/src/components/Navbar.vue";
 import countries from "/public/countries.json";
 import {ref,reactive} from "vue";
 import CountriesList from "/src/components/CountriesList.vue"

 const myCountries = Object.values(countries);

</script>

<style>

</style>