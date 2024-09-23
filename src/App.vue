<script setup>
import Map from "@/components/Map.vue"
</script>

<template>
  <div class="map__container">
    <Map/>
  </div>
</template>

<style>
body{
  display: flex;
  justify-content: center;
  align-items: center;
  .map__container{
    width:1200px;
    height: 700px;
    .map__element{
      width:100%;
      height:100%;
    }
  }
}

</style>
