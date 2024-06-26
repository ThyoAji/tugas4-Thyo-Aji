<template>
    <button @click="emitNewVideo">SEARCH</button>
  </template>
  
  <script>
  export default {
    name: 'GachaButton',
    methods: {
      emitNewVideo() {
        const videos = [
          { id: 'V2G8ESoDXm8', title: 'SZA - Saturn' },
          { id: 'Sv5yCzPCkv8', title: 'SZA - Snooze' },
          { id: 'SQnc1QibapQ', title: 'SZA - Kill Bill' },
          { id: 'HQPrprfg_FA', title: 'SZA - Far' },
          { id: 'npu0F7n4M9Y', title: 'SZA - Love Language' },
          { id: 'h-oGPR9jHtk', title: 'SZA - F2F' },
          { id: 'Z-T_O_vl-8Y', title: 'SZA - Low' },
          { id: 'w_6Ds6hr01M', title: 'SZA - Too Late' },
          { id: 'rA6DIHIg5To', title: 'SZA - Gone Girl' }
        ];
        const randomIndex = Math.floor(Math.random() * videos.length);
        const newVideo = videos[randomIndex];
        this.$emit('new-video', newVideo);
      }
    }
  }
  </script>
  
  <style>
  button {
    font-size: 1.5em;
    padding: 10px 20px;
    margin-top: 20px;
    cursor: pointer;
    background-color: #1E90FF;
    color: white;
    border: none;
    border-radius: 5px;
  }
  
  button:hover {
    background-color: #1C86EE;
  }
  </style>
  