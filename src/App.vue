<template>
  <div id="app">
    <h1>Contoh Nested Component + Emit + Slot</h1>
    <ParentComponent />
  </div>
</template>

<script setup>
import ParentComponent from './components/ParentComponent.vue'
</script>

<style>
/* Atasi default background putih dari body */
html, body {
  height: 100%;
  margin: 0;
  padding: 0;
  background-color: #121212; /* latar belakang gelap */
}

/* Root container */
#app {
  min-height: 100vh;
  padding: 20px;
}

/* Judul utama */
h1 {
  background-color: #000000;
  color: #000000; /* teks hitam */
  padding: 16px;
  border-radius: 12px;
  text-align: center;
  margin-bottom: 30px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
}
</style>




