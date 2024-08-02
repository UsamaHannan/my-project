<template>
    <v-container fluid>
    <v-row>
        <v-col cols="2">
<SideBar/>
        </v-col>

        <v-col cols="10" class="bg-grey-lighten-5"> 
<DestinationUi/>
        </v-col>
    </v-row>
    </v-container>
  </template>
  
  <script>
 

import DestinationUi from './DestinationUi.vue';
import SideBar from './SideBar.vue';
  export default {
    name: 'DestinationScreen',
    components: {
   
    
   SideBar,
   DestinationUi,
 },
    data: () => ({
      
          
    }),
  }
  </script>
  