<template>

  <div class="hero_container">
          
        <v-carousel cycle hide-delimiters>
            <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            reverse-transition="fade-transition"
            transition="fade-transition"
            >
            <v-row class="fill-height" align="center" title justify="center">
             <div>{{ item.title }}</div>
            </v-row>
            </v-carousel-item>
        </v-carousel>
        
        
    
  </div>
  
</template>

<script>
  export default {
    name: 'Hero',

   data () {
      return {
        items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
            title: 'Welcome to vuetify '
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
            title: 'Welcome to vuetify '
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
            title: 'Welcome to vuetify '
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
            title: 'Welcome to vuetify '
          },
        ],
      }
    },

  }
</script>
