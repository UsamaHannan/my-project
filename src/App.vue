<template>
  <v-app>
    <v-main>
      <DestinationScreen/>
    </v-main>
  </v-app>
</template>

<script>
import DestinationScreen from './components/DestinationScreen.vue';


export default {
  name: 'App',

  components: {
   
    
    DestinationScreen,
  },

  data: () => ({
    //
  }),
}
</script>
