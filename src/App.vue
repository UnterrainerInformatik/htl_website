<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs
          v-model="tab"
          align-with-title
        >
          <v-tabs-slider color="yellow"></v-tabs-slider>

          <v-tab>
            Start
          </v-tab>
          <v-tab>
            Pupils
          </v-tab>
          <v-tab>
            About
          </v-tab>
        </v-tabs>
      </template>
    </v-app-bar>

    <v-main>
      <v-tabs-items v-model="tab">
        <v-tab-item>
          <HelloWorld/>
        </v-tab-item>
        <v-tab-item>
          <Pupils
            :pupils="[
              { name: 'Ostermann Malte', text: 'Alter: 15 Jahre, Sitzplatz: 2, Geschlecht: Männlich.' },
              { name: 'Satzinger Niklas', text: '  Alter: 16 Jahre, Sitzplatz: 1, Geschlech: Männlich.' },
              { name: 'Yanik Kendler', text: '  Alter: 16 Jahre, Sitzplatz: 15, Geschlech: Männlich.' },
              { name: 'Michael Leisch', text: '  Alter: 17 Jahre, Sitzplatz: 16, Geschlech: Männlich.' },
              { name: 'Micheal Rueb', text: '  Alter: 16 Jahre, Sitzplatz: 13, Geschlech: Männlich.' }
              ]"
          />
        </v-tab-item>
        <v-tab-item>
          <About         
          />
        </v-tab-item>
      </v-tabs-items>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Pupils from './components/Pupils'
import About from './components/About'

export default {
  name: 'App',

  components: {
    HelloWorld,
    Pupils,
    About
  },

  data: () => ({
    tab: null
  }),
};
</script>
