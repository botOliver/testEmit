<script setup lang="ts">
import { ref } from 'vue'
const emit = defineEmits(['test-click'])
const counter = ref(0)

defineProps({
  newTest: {
    type: String,
    default: 'по дефолту'
  }
})

function testFunc() {
  emit('test-click', 'Проверено')
}
</script>

<template>
  <h1 @click="testFunc">{{ newTest }}</h1>
</template>

<style scoped></style>
