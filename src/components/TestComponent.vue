<script setup lang="ts">
import { ref } from 'vue'
const emit = defineEmits(['some-click'])
const counter = ref(0)

defineProps({
  msgTest: {
    type: String,
    default: 'HI'
  }
})

function testFunc() {
  emit('some-click', 'новый текст', counter.value++)
}
</script>

<template>
  <h1 @click="testFunc">{{ msgTest }} {{ counter }}</h1>
</template>

<style scoped></style>
