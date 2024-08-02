<template>

  <v-container>
    <v-row>
      <v-col>
        <div>
    <h1>Destination</h1>
   </div>
      </v-col>
      <v-col>
        <div class="d-flex justify-end">
          <v-btn
      @click="addDestination"
      color="#023C83"
   
      elevation="2"
      class="ma-2"
 
    >
      <v-icon left>mdi-plus</v-icon> <!-- Icon to the left of the text -->
      Add Destination
    </v-btn>
   </div>
      </v-col>
    </v-row>
    <div class="my-6">
      <v-card
    class="mx-auto"
    color="#023C83"
    max-width="600"
  >
    <v-card-text>
      <v-text-field
        :loading="loading"
        append-inner-icon="mdi-magnify"
        density="compact"
        label="Search Destination"
        variant="solo"
        hide-details
        single-line
        @click:append-inner="onClick"
      ></v-text-field>
    </v-card-text>
  </v-card>
    </div>
<div>
  <v-row class="my-4">
    <v-col>
      <div class="mt-3">
        <p class="text-grey-lighten-1"> Total Destinations found
        </p>
      </div>

    </v-col>
    <v-col>
<div class="d-flex justify-end">
  <v-menu 
    transition="scale-transition">
      <template v-slot:activator="{ props }">
        <v-btn
          
          v-bind="props"
          color="#023C83"
   prepend-icon="mdi-filter"
   elevation="2"
   class="ma-2"
   size="small"
        >
         Filter
        </v-btn>
      </template>
      <v-list>
        <v-list-item @click="filter('active')">
          <v-list-item-title>Active</v-list-item-title>
        
        </v-list-item>
        <v-list-item>
        
          <v-list-item-title>Inactive</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
</div>
    </v-col>
  </v-row>
</div>

<v-table>
    <thead>
      <tr>
        <th class="text-left font-weight-bold">
          Name
        </th>
        <th class="text-left font-weight-bold">
          Connector
        </th>
        <th class="text-left font-weight-bold">
          Source
        </th>
        <th class="text-left font-weight-bold">
          Last Sync
        </th>
        <th class="text-left font-weight-bold">
          Status
        </th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Snowflake</td>
        <td><v-icon color="#35aedd">mdi-snowflake</v-icon> <span>Snowflake</span></td>
        <td>Google Sheets</td>
        <td>8 days ago</td>
        <td>
          <v-btn
          variant="tonal"
          color="green"
          rounded
          size="small"
          
        >
          Active
        </v-btn>
        </td>
      </tr>
      <tr>
        <td>Cash</td>
        <td>put</td>
        <td>update</td>
        <td>get</td>
        <td>post</td>
      </tr>
      
    </tbody>
  </v-table>

 <div>
  
 </div>
  </v-container>
  
  
  
  </template>
  
  <script>
  
  export default {
    data: () => ({
      

      loaded: false,
      loading: false,
    }),

    methods: {
      onClick () {
        this.loading = true

        setTimeout(() => {
          this.loading = false
          this.loaded = true
        }, 2000)
      },
    },
  }
  </script>
  
  <style>

.v-field__append-inner{
  color: #023C83;
}
   

</style>