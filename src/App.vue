<template>
  <v-app :theme="theme">
    <v-app-bar
    elevation="0"
    >
      <v-row class="d-flex align-center pt-6">
        <v-col class="d-flex flex-row align-center justify-start mb-6">
          <v-img
          :src="theme === 'light' ? '../src/assets/Ativo 2GEO LOGO 2.png' : '../src/assets/Ativo 2GEO LOGO 1.png'"
          height="42"
          >
          </v-img>
          <v-spacer></v-spacer>
          <v-btn
            text>
              Home
            </v-btn>

            <v-btn text>
              About
            </v-btn>

            <v-btn text>
              Jobs
            </v-btn>
            <v-btn text>
              Skills
            </v-btn>
            <v-btn text>
              Contact
            </v-btn>
          <v-btn
            :prepend-icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"
            @click="onClick"
            rounded="pill"
            size="large"
            class="d-flex justify-center"
          ></v-btn>
        </v-col>
      </v-row>
      
    </v-app-bar>

    <v-main>
      <v-container>
        <HelloWorld></HelloWorld>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup lang="ts">
  import { ref } from 'vue'
  import HelloWorld from './components/HelloWorld.vue';
  {
    HelloWorld
  }
  const theme = ref('dark')

  function onClick () {
    theme.value = theme.value === 'light' ? 'dark' : 'light'
  }
  </script>