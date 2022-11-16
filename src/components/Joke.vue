<script setup>
	import { ref } from 'vue'


	const response = ref({})

  // adding delay
  await new Promise(resolve => {
    setTimeout(() => { 
      resolve()
    }, 1000)
  })
    
  try {
    const res = await fetch('https://v2.jokeapi.dev/joke/Any?blacklistFlags=nsfw,explicit,racist')
    console.log(res)
    response.value = (await res.json())
    console.log(response.value)
  } catch (error) {
    response.value = { answer: 'Error! Could not reach the API. ' + error, image: '' }
  }


  


</script>

<template>
  <p>{{ response.setup}}</p>
  <p>{{ response.delivery}}</p>
</template>

