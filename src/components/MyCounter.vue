<script setup>
import { ref } from 'vue'

let counter = ref(100)

let increment = () => {
  counter.value++
}
</script>

<template>
  <h1>{{ counter }}</h1>
  <input type="button" value="Increment" v-on:click="counter++" />
  <input type="button" value="Increment" @click="counter++" />
  <input type="button" value="Increment" @click="increment()" />
</template>

