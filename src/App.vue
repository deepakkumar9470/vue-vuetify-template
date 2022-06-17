<template>


   
     <div>
            <v-toolbar flat color="#5F7161" dark>
        <v-toolbar-title>DEEPAK KR</v-toolbar-title>

        <v-spacer></v-spacer>

      <v-toolbar-items> 
          <v-btn text>Home</v-btn>
          <v-btn text>Projects</v-btn>
          <v-btn text>About</v-btn>
          <v-btn text>Contact</v-btn>
         
      </v-toolbar-items>
    </v-toolbar>
    
    <v-content>    
        <Hero/>
        <Gallery/>
        <LatestPost/>
        <Contact/>
        
    </v-content>
 <v-footer>
     <Footer/>
 </v-footer>
    
     </div>

</template>


<script>
import Hero from '@/components/Hero.vue';
import Gallery from '@/components/Gallery.vue';
import LatestPost from './components/LatestPost.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';

export default {
    name: "App",
    components: { Hero, Gallery, LatestPost, Contact, Footer }
};
</script>

<style>
@import './style.css'
</style>