<template>
  <v-app>

    <!-- Nav bar -->
    <v-app-bar color="pink lighten-2" app dark>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <a class="nav-links-custom"><p class="mr-8 mt-4"><v-icon class="mr-2">mdi-email-outline</v-icon>info@dreamgirlfoundation.ngo</p></a>
      <a class="nav-links-custom"><p class="mr-4 mt-4"><v-icon class="mr-2">mdi-phone</v-icon>+919873133134</p></a>
    </v-app-bar>
    <!-- Nav drawer -->
    <v-navigation-drawer color="pink lighten-2" v-model="drawer" absolute temporary>
    <v-list>
      <v-list-item class="mt-3" v-for="item in content" :key="item.id">
        <a class="nav-links-custom">{{ item }}</a>
      </v-list-item>
    </v-list>        
  </v-navigation-drawer>
  <v-main>
      <LandingPage/>
  </v-main>
  </v-app>
</template>

<script>
import LandingPage from './components/LandingPage';

export default {
  name: 'App',
  
  components: {
    LandingPage,
  },

  data: () => ({
    drawer: false,
    content: ["Home", "Our Story", "Our Initiatives", "Get Involved", "Events & News", "Volunteer", "Donate", "COVID-19", "Contact Us"]
  }),
};
</script>

<style>
* {
  font-family: Arial, Helvetica, sans-serif;
}

.nav-links-custom {
  color: white !important;
}

@media screen and (max-width: 600px) {
  .nav-links-custom {
    font-size: 10px;
  }
}
</style>