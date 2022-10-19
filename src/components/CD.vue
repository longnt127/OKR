<template>
  <div class="cd">
    <div class="cd-thumb" :style="{'background-image': `url(${songs[1].image})`,}"></div>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType, computed } from "vue";
import Song from '@/types/Song'

export default defineComponent({
  name: "CD",
  props: {
    songs: {
      type: Array as PropType<Song[]>,
      required: true
    }
  },
  setup(props) {
    const songs = computed(() => {
      return [...props.songs]
    })
    return songs
  }
 });

</script>

<style></style>
