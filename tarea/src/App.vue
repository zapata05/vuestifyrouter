<template>
 <v-app id="inspire">
    <v-navigation-drawer v-model="drawer">

      <RouterView></RouterView>
     
    </v-navigation-drawer>

    <v-app-bar>
      
      <v-app-bar-nav-icon @click="drawer = !drawer">
      
      </v-app-bar-nav-icon>
<RouterLink to="/"></RouterLink>
      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-main>
     
    </v-main>
  </v-app>
</template>

<script setup>
  import { ref } from 'vue'

  const drawer = ref(null)
</script>

<script>
  export default {
    data: () => ({ drawer: null }),
    components: { RouterLink, RouterView }
}
</script>