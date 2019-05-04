<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Vuetify</span>
        <span class="font-weight-light">Spreed Sheet</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        flat
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">Latest Release</span>
      </v-btn>
    </v-toolbar>

    <v-content>
      <Container/>
    </v-content>
    <tfxi :name="'farhoud'"></tfxi>
  </v-app>
</template>

<script>
import Container from './components/Container'
import tfxi from './components/tfxi'

export default {
  name: 'App',
  components: {
      Container,
      tfxi
  },
  data () {
    return {
      //
    }
  }
}
</script>
