<template>
  <div class="parent">
    <p>Ini Parent Component</p>
    <p><strong>Pesan dari Child:</strong> {{ pesan }}</p>

    <ChildComponent @kirim="terimaDariChild">
      <template #default>
        <p><em>Ini konten dari Parent ke slot Child</em></p>
      </template>
    </ChildComponent>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

const pesan = ref('')

const terimaDariChild = (data) => {
  pesan.value = data
}
</script>

<style scoped>
.parent {
  background-color: #2c2b3f; /* ungu gelap lembut */
  border-radius: 16px;
  padding: 24px;
  margin: 20px auto;
  max-width: 700px;
  color: #d0d0d0;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.4);
  transition: transform 0.3s;
}

.parent:hover {
  transform: scale(1.01);
}

.parent p {
  font-size: 17px;
  color: #e2e2e2;
}
</style>




