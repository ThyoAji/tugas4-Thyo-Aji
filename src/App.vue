<template>
  <div id="app">
    <h1>SZA SONG</h1>
    <GachaButton @new-video="changeVideo"></GachaButton>
    <VideoDisplay :videoId="currentVideoId" :title="currentVideoTitle"></VideoDisplay>
  </div>
</template>

<script>
import GachaButton from './components/GachaButton.vue';
import VideoDisplay from './components/VideoDisplay.vue';

export default {
  name: 'App',
  components: {
    GachaButton,
    VideoDisplay
  },
  data() {
    return {
      currentVideoId: 'V2G8ESoDXm8',  // Video default
      currentVideoTitle: 'SZA - Saturn'
    }
  },
  methods: {
    changeVideo(newVideo) {
      this.currentVideoId = newVideo.id;
      this.currentVideoTitle = newVideo.title;
    }
  }
}
</script>

<style>
html, body {
  height: 100%;
  margin: 0;
  padding: 0;
}

#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  background-image: url('https://r4.wallpaperflare.com/wallpaper/69/490/463/sza-ocean-view-women-hd-wallpaper-29c0987db1baad2bf6f7589fe0a1a64d.jpg');
  background-size: cover;
  background-position: center;
}

h1 {
  color: white;
  text-align: center;
  margin-bottom: 20px;
}
</style>
