<template>
  <div class="container-watches">
    <AppWatch />
    <AppWatch timeZone="ko-KR" color="blue" />
    <AppWatch timeZone="ar-EG" color="pink" />
  </div>
</template>

<script>
// @ is an alias to /src
import AppWatch from '@/components/AppWatch.vue'

export default {
  name: 'App',
  components: {
    AppWatch
  }
}
</script>

<style>
.container-watches {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
</style>
