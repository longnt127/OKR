<template>
    <div class="playlist">
        <div class="song" v-for="(song, index) in songs" :key="index">
            <div class="thumb" :style="{ 'background-image': `url(${song.image})` }"></div>
            <div class="body">
                <h3 class="title">{{ song.name }}</h3>
                <p class="author">{{ song.singer }}</p>
            </div>
            <div class="option">
                <i class="fas fa-ellipsis-h"></i>
            </div>
        </div>
    </div>
    
</template>

<script lang="ts">
import { computed, defineComponent, PropType, ref, onMounted } from "vue";
import Song from "@/types/Song";

export default defineComponent({
    name: "Play-list",
    props: {
        songs: {
            type: Array as PropType<Song[]>,
            required: true,
        },
    },
    setup(props) {
        const songs = computed(() => {
            return [...props.songs];
        });
        return songs;
    }
});
</script>

<style>
</style>
