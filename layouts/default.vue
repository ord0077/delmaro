<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      dense
      flat
      class="primary"
      dark
    >
      <v-btn icon @click.stop="fixed = !fixed">
        <v-icon small>mdi-email</v-icon>
      </v-btn>

      <span v-text="title"></span>

      <v-spacer />
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon small>mdi-whatsapp</v-icon>
      </v-btn>

      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon small>mdi-phone</v-icon>
      </v-btn>

      <span>03108559858</span>
    </v-app-bar>

    <v-toolbar class="mt-12" height="120px">
      <div>
        <v-img
          max-width="120px"
          src="https://delmaro.nl/wp-content/uploads/2020/10/delmaro_logo_optimize.png"
        />
      </div>

      <v-spacer />

      <div>
        <span class="pa-2">Home</span>
        <span class="pa-2">Winkel</span>
        <span class="pa-2">Neem Contact Op</span>
      </div>
    </v-toolbar>

    <v-carousel hide-delimiters>
      <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src">
        <div>
          <div
            v-if="i == 0"
            dark
            class="mt-15 sliderSection sliderSection1 success lighten-2"
          >
            one
          </div>
          <div
            v-if="i == 2"
            dark
            class="mt-15 sliderSection sliderSection3 error"
          >
            one
          </div>
        </div>
      </v-carousel-item>
    </v-carousel>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

    <!-- <v-footer
      dark
      class="mt-5"
      app
    >
     <v-col cols="3">
         <div>

        <v-img max-width="120px" src="https://delmaro.nl/wp-content/uploads/2020/10/delmaro_logo_optimize.png" />
      </div>
      </v-col>
       <v-col cols="3">
         {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
       <v-col cols="3">
         {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
       <v-col cols="3">
         {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>

      <v-col cols="12">
         {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
    </v-footer> -->

    <v-footer dark class="grey darken-4" :absolute="!fixed" app>
      <v-col cols="3"
        ><v-img
          max-width="120px"
          src="https://delmaro.nl/wp-content/uploads/2020/10/delmaro_logo_optimize.png"
        />
        <span class="display-24"
          >Delmaro is al jaren een vertrouwde naam als het gaat om de import en
          export van Zuid Amerikaanse en Latijnse delicatessen.</span
        >
        <p>
          Al langer dan 10 jaar heeft onze groothandel kwaliteit én service hoog
          in het vaandel staan.
        </p>
      </v-col>
      <v-col cols="3">Contact Us
   <ul> <span class="sx-1" > Telefoon 085 444 4710 </span></ul>
 <ul> <span class="sm-1"> Telefoon 085 444 4710 </span> </ul>

      </v-col>

      <v-col cols="3">Useful Links</v-col>
      <v-col cols="3">Product Categories</v-col>

      {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          src: "http://198.13.33.71/delmaro/wp-content/uploads/2021/06/slider2.png",
        },
        {
          src: "http://198.13.33.71/delmaro/wp-content/uploads/2021/06/slider1.png",
        },
        {
           src: "http://198.13.33.71/delmaro/wp-content/uploads/2021/06/slider2.png",
        },
        {
          src: "http://198.13.33.71/delmaro/wp-content/uploads/2021/06/slider1.png",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
    };
  },
};
</script>

<style>
.sliderSection {
  width: 50%;
  height: 150px;
  color: white;
}

.sliderSection1 {
  opacity: 0.9;
}

.sliderSection3 {
  opacity: 0.5;
}
</style>
