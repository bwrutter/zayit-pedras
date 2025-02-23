<template>
  <v-container>
    <v-sheet height="200">
      <v-img
        :src="randomImage"
        height="200"
        cover
      ></v-img>
    </v-sheet>
  </v-container>
</template>

<script setup>
import { ref, onMounted } from "vue";

const randomImage = ref("");

onMounted(() => {
  randomImage.value = `https://picsum.photos/1200/400?random=${Math.random()}`;
});
</script>
