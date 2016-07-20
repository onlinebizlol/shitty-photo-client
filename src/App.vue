<template>
    <div id="shitty-photo" :style="{ 'background-image': 'url(' + shittyPhoto + ')' }"></div>
</template>

<script>
// FIXME make it so we don't have to do this
var NUM_PHOTOS = 2;

export default {
  data () {
    return {}
  },

  computed: {
    shittyPhoto () {
      var rindex = Math.floor(Math.random() * NUM_PHOTOS);

      return `src/assets/images/shitty-${rindex}.jpg`;
    }
  }
}
</script>

<style>
html {
  width: 100%;
  height: 100%;
  background-color: black;
}

body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

#shitty-photo {
  width: 100%;
  height: 100%;
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}
</style>
