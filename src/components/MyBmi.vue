<template>
  <div>
    My BMI
    <label for="weight">Weight (kg):</label>
    <input id="weight" v-model.number="weight" type="number" />
    <label for="height">Height (cm):</label>
    <input id="height" v-model.number="height" type="number" />
    <p>BMI: {{ bmi.toFixed(2) }}</p>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
const weight = ref(0)
const height = ref(0)
const bmi = computed(() => {
  const heightInMeters = height.value / 100
  if (!weight.value || !heightInMeters) return 0

  return weight.value / (heightInMeters * heightInMeters)
})
</script>
