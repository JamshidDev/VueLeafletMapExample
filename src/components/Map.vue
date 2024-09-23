<template>
  <div class="map__element" id="map_element"></div>
</template>

<script setup>
import {ref, onMounted} from 'vue'
import L from 'leaflet';


const map = ref(null)
const mapView = ref({
  center:[41.311081,69.240562],
  zoom:12,
  options:{
    maxZoom: 18,
    minZoom:5,
    attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>',
    zoomAnimation:true,
  }
})



const initialMap = ()=>{
  map.value = L.map('map_element').setView(mapView.value.center, mapView.value.zoom);
  L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', mapView.value.options).addTo(map.value);
}









onMounted(async ()=>{
  initialMap()
})
</script>


