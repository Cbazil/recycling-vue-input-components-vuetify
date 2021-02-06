<template>
  <v-app>
    <Header />
    <v-main>
      <h1>Landing Page</h1>
    </v-main>
  </v-app>
</template>

<script>
import Header from './components/Header'
export default {
  name: 'App',
  components: {
    Header
  },

  data: () => ({
    //
  }),
};
</script>
