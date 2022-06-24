<template>
 <v-app id="inspire">
    <v-app-bar
          app
          color="white"
          flat
        >
      <v-container class="py-0 fill-height">
        <v-avatar
          class="mr-10"
          color="grey darken-1"
          size="32"
         
        > <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="Ahsan"
      /></v-avatar>

        <v-btn
          v-for="link in links"
          :key="link"
          text
        >
          {{ link }}
        </v-btn>

        <v-spacer></v-spacer>

        <v-responsive max-width="300">
          <v-text-field
            dense
            autofocus="true"
            flat
            hide-details
            outlined
            rounded
            solo-inverted
            placeholder="Search"
            append-icon="mdi-magnify"
          ></v-text-field>
          
        </v-responsive>
      </v-container>
    </v-app-bar>
    </v-app>
</template>


<script>
  export default {
    data: () => ({
      links: [
        'Dashboard',
        'Profile',
        'Products',
        'Orders',
        'System Setting'
      ],
    }),
  }
</script>

<style>


</style>