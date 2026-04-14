<template>
  <div class="q-pa-md">
    <div class="q-gutter-y-md">
      <q-option-group
        v-model="panel"
        inline
        :options="[
          { label: 'Info', value: 'info' },
          { label: 'My art', value: 'art' },
          { label: 'Dual Elemental', value: 'videogames' },
          { label: 'Map', value: 'map' }
        ]"
      />

      <q-tab-panels v-model="panel" animated class="shadow-2 rounded-borders">
        <q-tab-panel name="info">
          <div class="text-h6 q-mb-md">About me</div>
          <div class="row">
            <div class="col-3">
              <q-img
                src="public/img/profile.jpg"
                alt="Jordi Gomara"
                class="q-mb-md"
                style="width: 190px; height: 190px; border-radius: 70%"
              />
            </div>
            <div class="col-9">
              Developer of applications with more than four years of work experience in both the public and private sectors.
              Full Stack programmer focused on data management applications, including graphics and geospatial map visualizations.
              Data scientist, sprite designer, video editor, video game developer, and oil painting artist.
            </div>
          </div>
        </q-tab-panel>

        <q-tab-panel name="art">
          <div class="text-h6">My art</div>
          <div class="q-mb-md"> Gallery of oil paintings I have done over the years. </div>
          <q-img
            src="public/art/IMG_20250914_214406_775.jpg"
            alt="Art 1"
            class="q-mb-md"
            style="width: 450px; height: 550px; border-radius: 10%"
          />
        </q-tab-panel>

        <q-tab-panel name="videogames">
          <div class="text-h6">Dual Elemental</div>
          <q-video
            :ratio="16/7"
            src="https://www.youtube.com/embed/2gVLFwD4QkE?si=SaC8wwiHbIitVjqm"
          />
        </q-tab-panel>

        <q-tab-panel name="map">
          <div class="text-h6">Leaflet Map</div>
          <MapComponent></MapComponent>
        </q-tab-panel>
      </q-tab-panels>
    </div>
  </div>
</template>

<script>
import { defineComponent, ref } from 'vue'

import MapComponent from 'components/MapComponent.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    MapComponent
  },
  setup () {
    const panel = ref('info')
    return {
      panel
    }
  }
})
</script>
