<template>
    <div>
      <h2>{{ title }}</h2>
      <iframe
        :src="'https://www.youtube.com/embed/' + videoId"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
        width="560"
        height="315"
      ></iframe>
    </div>
  </template>
  
  <script>
  export default {
    name: 'VideoDisplay',
    props: {
      videoId: {
        type: String,
        required: true
      },
      title: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style>
  h2 {
    color: white;
  }
  
  iframe {
    margin-top: 20px;
  }
  </style>
  