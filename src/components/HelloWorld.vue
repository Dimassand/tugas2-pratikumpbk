<template>
  <div>
    <!-- Isi komponen HelloWorld di sini -->
    <input
      v-model="text"
      placeholder="apa yang ada ingin masukkan..."
      :style="{ 'font-weight': text.length > 5 ? 'bold' : 'normal' , color: text.length > 5 ? 'blue' : 'black' }"
    />
    <p v-if="text.length > 0">Panjang teks: {{ text.length }}</p>
    
  </div>
</template>

<script setup>
import { ref, defineExpose } from "vue";

// Mendefinisikan variabel reaktif text
const text = ref("");

// Mengekspos variabel text untuk akses dari luar komponen
defineExpose({ text });
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>