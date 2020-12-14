<template>
  <v-app>
    <v-main>
      <v-container>
        <h1 class="text-center">Axios Dolar</h1>
        <Home/>
        <v-dialog
            v-model="loading.estado"
            hide-overlay
            persistent
            width="300"
          >
            <v-card
              :color="loading.color"
              dark
            >
             <v-card-text>
          {{loading.titulo}}
          <v-progress-linear
            indeterminate
            color="white"
            class="mb-0"
          ></v-progress-linear>
        </v-card-text>
      </v-card>
    </v-dialog>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import {mapState} from 'vuex'
import Home from './views/Home.vue'
export default {
  name: 'App',

  components: {
    Home
  },

  data (){
    //
    return {

    }
  },
  computed: {
    ...mapState(['loading'])
  }
};
</script>
