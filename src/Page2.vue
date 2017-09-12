<template>
  <v-ons-page>
    <custom-toolbar :back-label="'Page 1'">Page 2</custom-toolbar>
    <p style="text-align: center">This is the second page</p>
<div id="app">
  <div class="map-container">
    <gmap-map :center="{lat:1.38, lng:103.8}" :zoom="12">
      <gmap-marker :position="{lat:1.38, lng:103.8}">
      </gmap-marker>
      <gmap-info-window :position="{lat:1.38, lng:103.8}">
        Hello world!
      </gmap-info-window>
    </gmap-map>
  </div>
</div>

  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar';
  import app from './App';

  export default {
    methods: {
      pop() {
        this.pageStack.pop();
      } 
    },
    props: ['pageStack'],
    components: { customToolbar }
  }
</script>

