<template>
  <v-app class="pa-4">
    <v-main>
      <h3>Working :</h3>
      <v-carousel
        hide-delimiter-background
        cycle
        interval="8000"
        show-arrows="hover"
      >
        <v-carousel-item
          v-for="project in projects"
          :key="project.id"
          src="@/assets/img/test.jpg"
        >
          <v-card
            variant="outlined"
            style="backdrop-filter: blur(4px);"
          >
            <v-card-title>
              <h3>{{ project.name }}</h3>
            </v-card-title>

            <v-card-text>
              <p>{{ project.description }}</p>
            </v-card-text>
          </v-card>
        </v-carousel-item>
      </v-carousel>

      <v-divider class="my-4" />

      <h3>Not working :</h3>
      <v-carousel
        hide-delimiter-background
        cycle
        interval="8000"
        show-arrows="hover"
      >
        <v-carousel-item
          v-for="project in projects"
          :key="project.id"
          :src="project.image"
        >
          <v-card
            variant="outlined"
            style="backdrop-filter: blur(4px);"
          >
            <v-card-title>
              <h3>{{ project.name }}</h3>
            </v-card-title>

            <v-card-text>
              <p>{{ project.description }}</p>
            </v-card-text>
          </v-card>
        </v-carousel-item>
      </v-carousel>
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from "vue"

const projects = ref([
  {
    id: 1,
    name: "Test 1",
    description: "BlaBla",
    image: "@/assets/img/test.jpg"
  },
  {
    id: 2,
    name: "Test 2",
    description: "BlaBla",
    image: "@/assets/img/test.jpg"
  },
  {
    id: 3,
    name: "Test 3",
    description: "BlaBla",
    image: "@/assets/img/test.jpg"
  }
])
</script>
