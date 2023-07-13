<script setup>
import { ref } from 'vue'

let person = ref()

let makeApiCall = async () => {
  let url = `https://jsonplaceholder.typicode.com/posts/1`
  let res = await fetch(url)
  let data = await res.json()

  person.value = data
}
</script>

<template>
  <h1>My API</h1>
  <input type="button" value="API CALL" @click="makeApiCall" />

  <h1>{{ person }}</h1>
  <h1>{{ person?.title }}</h1>
</template>