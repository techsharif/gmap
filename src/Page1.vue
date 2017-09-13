<template>
<v-ons-page>
<div id="app">
<gmap-map
    :center="center"
    :zoom="7"
    style="width: 500px; height: 300px"
  >
    <gmap-marker
      :key="index"
      v-for="(m, index) in markers"
      :position="m.position"
      :clickable="true"
      :draggable="true"
      @click="center=m.position"
    ></gmap-marker>
  </gmap-map>
</div>
</v-ons-page>
</template>

<script>
  import * as VueGoogleMaps from 'vue2-google-maps';
  import Vue from 'vue';
Vue.use(VueGoogleMaps, {
  load: {
    key: 'AIzaSyDX3SEHwFUY-k_Jp7YMp0-uTvo7up-paXM'
  }
});

export default {
  data () {
    return {
    center: {lat: 10.0, lng: 10.0},
        markers: [{
          position: {lat: 10.0, lng: 10.0}
        }, {
          position: {lat: 11.0, lng: 11.0}
        }]
}
}
}
</script>

