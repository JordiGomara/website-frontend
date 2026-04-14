<template>
  <iframe
    id="map"
    title="map"
    width="100%"
    height="1000px"
    src="https://mapes.salt.cat/#/share/?c=41.978124,2.790763&z=15&la=simple&l=g21.14"
  />
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'MapComponent',
})
</script>
