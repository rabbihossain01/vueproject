<template>
  <div class="container">
    <button @click="componentToRnder = 'compHome'">Home</button>
    <button @click="componentToRnder = 'compAbout'">About</button>
    <button @click="componentToRnder = 'compContact'">Contacat</button>
    
    <keep-alive>
       <component :is="componentToRnder"></component>
    </keep-alive>
   

  </div>
</template>
 <script>

 import compHome from "./Components/Home"
 import compAbout from "./Components/About"
 import compContact from "./Components/Contact"
 export default {
   data(){
     return {
       componentToRnder:"compHome"
     }

   },
   components:{
     compHome,
     compAbout,
     compContact
   }
   
 }
 </script>