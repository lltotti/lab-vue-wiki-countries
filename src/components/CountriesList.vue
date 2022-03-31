<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup



 import countries from "/public/countries.json";
 import {ref,reactive} from "vue";

 const myCountries = Object.values(countries);


 
//  const fiveContacts = reactive(myContacts.slice(0,5));
//  const restContacts = reactive(myContacts.slice(5,myContacts.length));
 
 

</script>

<template>
  <div>
  <table style="margin-left: auto;  margin-right: auto;">
    <tr>
      <th style="padding:10px;">COUNTRY</th>
    </tr>
    <tr v-for="country in myCountries" :key="country.alpha3Code" :id="country.alpha3Code">
        <td style="padding:10px;">
            <div>
                <img :src="'https://flagpedia.net/data/flags/icon/72x54/'+country.alpha2Code.toString().toLowerCase()+'.png'" style="width:60px;">
                <p> {{country.name.official}} </p>

            </div>
        </td>


    </tr>
    
  </table>

  </div>

</template>

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
