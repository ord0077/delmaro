<template>
 <div>
    <v-row>
    <v-col class="text-center">
     <h1> Over ons</h1>
      <blockquote class="blockquote">
        Delmaro is al jaren een vertrouwde naam als het gaat om de import en export van Zuid-Amerikaanse en Latijnse lekkernijen. Al meer dan 10 jaar stelt onze groothandel kwaliteit en service hoog in het vaandel. Op het gebied van verse kruiden, specerijen, groenten en andere producten uit deze landen fungeert de Delmaro-groothandel als de poort naar Europa.
        <v-divider class="ma-5" color="#F98E45"></v-divider>
      </blockquote>
    </v-col>
  </v-row>

   <v-row>
    <v-col class="text-center">
      <img
        src="https://delmaro.nl/wp-content/uploads/2020/08/salsas.png"
        alt="salsas"
        class="mb-5"
      >

    </v-col>

    <v-col class="text-center">
      <img
        src="https://delmaro.nl/wp-content/uploads/2020/08/Otros-banner.png"
        alt="Otros"
        class="mb-5"
      >

    </v-col>
  </v-row>

    <v-row>
    <v-col class="text-center">
     <h1>Nieuwste Producten</h1>

      <v-toolbar flat class="mt-5">
    <v-tabs
      v-model="tab"
      flat
      centered
      class="mb-5"
    >
      <v-tabs-slider></v-tabs-slider>

      <v-tab href="#tab-1">
        Vinager

      </v-tab>

      <v-tab href="#tab-2">
        Chiles

      </v-tab>

      <v-tab href="#tab-3">
        Chili Pasta

      </v-tab>

      <v-tab href="#tab-4">
        Chili Sauces

      </v-tab>
    </v-tabs>
  </v-toolbar>


        <v-tabs-items v-model="tab">
      <v-tab-item
        v-for="i in 4"
        :key="i"
        :value="'tab-' + i"
      >

          <v-row v-if="i == 1 || i == 4">
          <v-col cols="6">
          <v-card flat>
          <v-card-text>
            <v-img src="https://delmaro.nl/wp-content/uploads/2018/04/WhiteVinegar.png"></v-img>
          </v-card-text>
          </v-card>

          </v-col>

          <v-col cols="6">
          <v-card flat>
           <v-card-text>
            <v-img src="https://delmaro.nl/wp-content/uploads/2018/04/AppleVinegar.png"></v-img>
          </v-card-text>
          </v-card>

          </v-col>
          </v-row>

          <v-row v-if="i == 2 || i == 4">
          <v-col cols="6">
          <v-card flat>
          <v-card-text>
            <v-img src="https://delmaro.nl/wp-content/uploads/2018/04/Nachos_de_Jalapen%CC%83o_12oz.png"></v-img>
          </v-card-text>
          </v-card>

          </v-col>

          <v-col cols="6">
          <v-card flat>
           <v-card-text>
            <v-img src="https://delmaro.nl/wp-content/uploads/2018/04/Chiles_Jalapen%CC%83os_en_Escabeche_7oz.png"></v-img>
          </v-card-text>
          </v-card>

          </v-col>
          </v-row>


           <v-row v-if="i == 3 || i == 4">
          <v-col cols="6">
          <v-card flat>
          <v-card-text>
            <v-img src="https://delmaro.nl/wp-content/uploads/2020/09/AnchoPaste_Producto.png"></v-img>
          </v-card-text>
          </v-card>

          </v-col>

          <v-col cols="6">
          <v-card flat>
           <v-card-text>
            <v-img src="https://delmaro.nl/wp-content/uploads/2020/09/AnchoPaste_Producto.png"></v-img>
          </v-card-text>
          </v-card>

          </v-col>

          <v-col cols="6">
          <v-card flat>
           <v-card-text>
            <v-img src="https://delmaro.nl/wp-content/uploads/2020/09/AnchoPaste_Producto.png"></v-img>
          </v-card-text>
          </v-card>

          </v-col>

          </v-row>
      </v-tab-item>
    </v-tabs-items>
     </v-col>
   </v-row>

   <v-row>
     <v-col cols="4">
         <v-img src="https://delmaro.nl/wp-content/uploads/2018/04/WhiteVinegar.png"></v-img>
     </v-col>
      <v-col cols="4">
         <v-img src="https://delmaro.nl/wp-content/uploads/2018/04/WhiteVinegar.png"></v-img>
     </v-col>
      <v-col cols="4">
         <v-img src="https://delmaro.nl/wp-content/uploads/2018/04/WhiteVinegar.png"></v-img>
     </v-col>
   </v-row>


 </div>
</template>

<script>
  export default {
    data () {
      return {
        tab: null,
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      }
    },
  }
</script>
