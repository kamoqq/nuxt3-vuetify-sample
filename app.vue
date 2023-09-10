<script setup lang="ts">
import { useTheme, useDisplay } from 'vuetify'

const theme = useTheme()
const { smAndDown } = useDisplay()

function toggleTheme () {
  theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
}
</script>

<template>
  <v-app>
    <v-container>
      <v-btn @click="toggleTheme" :width="smAndDown ? '100%' : undefined">toggle theme</v-btn>
    </v-container>
  </v-app>
</template>
