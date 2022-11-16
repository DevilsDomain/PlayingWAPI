<script setup>
import HelloWorld from './components/Joke.vue'
</script>

<template>
  <Suspense>
    <HelloWorld/>
    <template #fallback>
      <img src="https://media.tenor.com/o8m3bKTsifUAAAAC/hold-on.gif" />
    </template>
  </Suspense>
  
</template>
