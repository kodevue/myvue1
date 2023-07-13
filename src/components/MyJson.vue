<script setup>
import { ref } from 'vue'

let person = ref({ name: 'mumbai', id: 1, counter: 100 })

let increment = () => {
  person.value.counter++
}
</script>

<template>
  <h1>My JSON</h1>

  <h1>{{ person.id }} / {{ person.name }} / {{ person.counter }}</h1>
  <input type="button" value="Inc" @click="person.value.counter++" />
  <input type="button" value="Inc" @click="increment" />
</template>