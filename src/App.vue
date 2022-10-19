<template>
  <div id="app">
    <div class="player">
      <!-- Dashboard -->
      <div class="dashboard">
        <!-- Header -->
        <header>
          <h4>Now playing:</h4>
          <h2>String 57th & 9th</h2>
        </header>

        <!-- CD -->
        <CD :songs="songs" />

        <!-- Control -->
        <Control />

      </div>

      <!-- Playlist -->
      <Playlist :songs="songs" />
    </div>
    <audio id="audio" src="https://filesamples.com/samples/audio/mp3/sample1.mp3" />
  </div>

</template>

<script lang="ts">

import { defineComponent, ref } from 'vue';
import CD from './components/CD.vue'
import Playlist from './components/Playlist.vue'
import Control from './components/Control.vue'
import Song from './types/Song'

export default defineComponent({
  name: 'App',
  components: {
    CD, Playlist, Control
  },
  setup() {
    const songs = ref<Song[]>([
      { name: 'Damn', singer: 'Raftaar x kr$na', path: 'https://filesamples.com/samples/audio/mp3/sample1.mp3', image: 'https://a10.gaanacdn.com/gn_img/albums/YoEWlabzXB/oEWlj5gYKz/size_xxl_1586752323.webp' },
      { name: 'Damn', singer: 'Raftaar x kr$na', path: 'https://filesamples.com/samples/audio/mp3/sample1.mp3', image: 'https://a10.gaanacdn.com/gn_img/albums/YoEWlabzXB/oEWlj5gYKz/size_xxl_1586752323.webp' },
      { name: 'Damn', singer: 'Raftaar x kr$na', path: 'https://filesamples.com/samples/audio/mp3/sample1.mp3', image: 'https://a10.gaanacdn.com/gn_img/albums/YoEWlabzXB/oEWlj5gYKz/size_xxl_1586752323.webp' },
      { name: 'Damn', singer: 'Raftaar x kr$na', path: 'https://filesamples.com/samples/audio/mp3/sample1.mp3', image: 'https://a10.gaanacdn.com/gn_img/albums/YoEWlabzXB/oEWlj5gYKz/size_xxl_1586752323.webp' },
      { name: 'Damn', singer: 'Raftaar x kr$na', path: 'https://filesamples.com/samples/audio/mp3/sample1.mp3', image: 'https://a10.gaanacdn.com/gn_img/albums/YoEWlabzXB/oEWlj5gYKz/size_xxl_1586752323.webp' },
      { name: 'Damn', singer: 'Raftaar x kr$na', path: 'https://filesamples.com/samples/audio/mp3/sample1.mp3', image: 'https://a10.gaanacdn.com/gn_img/albums/YoEWlabzXB/oEWlj5gYKz/size_xxl_1586752323.webp' },
      { name: 'Damn', singer: 'Raftaar x kr$na', path: 'https://filesamples.com/samples/audio/mp3/sample1.mp3', image: 'https://a10.gaanacdn.com/gn_img/albums/YoEWlabzXB/oEWlj5gYKz/size_xxl_1586752323.webp' }
    ])

    return { songs }
  }
});

</script>

<style>

</style>
