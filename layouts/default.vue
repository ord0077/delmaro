<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      dense
      flat
      color="#F98E45"
      dark

    >
      <v-btn
        icon
        @click.stop="fixed = !fixed"
      >
        <v-icon small>mdi-email</v-icon>

      </v-btn>

       <span v-text="title"></span>

      <v-spacer />
      <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon small>mdi-whatsapp</v-icon>
      </v-btn>

       <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon small>mdi-phone</v-icon>


      </v-btn>

      <span>03108559858</span>


    </v-app-bar>


    <v-toolbar class="mt-12" height="120px">

      <div class="">

       <v-img max-width="120px" src="https://delmaro.nl/wp-content/uploads/2020/10/delmaro_logo_optimize.png" />
      </div>

      <v-spacer />

      <div>

        <span class="pa-2">Home</span>
        <span class="pa-2">Winkel</span>
        <span class="pa-2">Neem Contact Op</span>
      </div>
    </v-toolbar>

    <v-carousel hide-delimiters>
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
      >


      <div>
        <div v-if="i == 0" dark :class="`mt-15 sliderSection1`">one</div>
        <div v-if="i == 2" dark :class="`mt-15 sliderSection3`">one</div>
      </div>


       </v-carousel-item>
    </v-carousel>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style>
  .sliderSection1 {

    width:50%;
    height:150px;
    background:#A9D04F;
    opacity:0.9;
    color:white;
  }

  .sliderSection3 {

    width:50%;
    height:150px;
    background:red;
    opacity:0.5;
    color:white;
  }


</style>
