<template>
  <div class="child">
    <p>Ini dari Child Component</p>
    <button @click="kirimKeParent">Kirim Data ke Parent</button>
    <slot></slot> <!-- slot akan diisi dari parent -->
  </div>
</template>

<script setup>
import { defineEmits } from 'vue'
const emit = defineEmits(['kirim'])

const kirimKeParent = () => {
  emit('kirim', 'Halo dari Child!')
}
</script>

<style scoped>
.child {
  background-color: #3a3a52; /* biru keunguan gelap */
  border-radius: 12px;
  padding: 20px;
  margin-top: 24px;
  color: #f0f0f0;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s;
}

.child:hover {
  transform: translateY(-3px);
}

.child button {
  background-color: #f39c12;
  color: #fff;
  font-weight: bold;
  border: none;
  padding: 10px 18px;
  border-radius: 8px;
  cursor: pointer;
  margin-top: 12px;
  transition: background-color 0.3s;
}

.child button:hover {
  background-color: #e67e22;
}
</style>




