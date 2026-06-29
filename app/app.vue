<template>
  <UApp>
    <NuxtPage />
  </UApp>
</template>

<script setup>
definePageMeta({
  colorMode: 'dark',
})
const colormode = useColorMode()
colormode.preference = 'dark'


</script>