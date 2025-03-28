<script setup>
import InputNumber from './volt/InputNumber.vue'
import { ref } from 'vue'

const value = ref(4)
</script>

<template>
  <div
    class="bg-surface-50 dark:bg-surface-950 min-h-screen flex items-center justify-center p-8"
  >
    <div class="bg-white dark:bg-gray-800 flex flex-col items-center justify-center gap-3 shadow-lg rounded-2xl p-6 w-96">
      <h2>Without any pt, works fine</h2>
      <InputNumber v-model="value" />
      <h2>With pt:root:class="text-red", works fine</h2>
      <InputNumber v-model="value" pt:root:class="text-xl" />
      <h2>with pt:pcInputText:root:class="text-xl", doesn't work</h2>
      <InputNumber v-model="value" pt:pcInputText:root:class="text-xl" />
    </div>
  </div>
</template>
