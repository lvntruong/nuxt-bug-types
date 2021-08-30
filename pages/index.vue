<!-- @format -->

<template>
  <Tutorial />
</template>

<script lang="ts">
import Vue from "vue";

import { Loader } from '@googlemaps/js-api-loader';

const loader = new Loader({
  apiKey: "",
  version: "weekly"
});

loader
  .load()
  .then((google) => {
    new google.maps.DistanceMatrixService();
  })
  .catch(e => {
    // do something
  });

export default Vue.extend({});
</script>
