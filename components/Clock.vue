<!-- components/Clock.vue -->
<template>
    <div>
      <h2>Current Time:</h2>
      <p>{{ currentTime }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentTime: this.getCurrentTime(),
      };
    },
    methods: {
      getCurrentTime() {
        return new Date().toLocaleTimeString();
      },
      updateTime() {
        this.currentTime = this.getCurrentTime();
        this.$forceUpdate(); // Force update to trigger reactivity
      },
    },
    mounted() {
      // Update time every second
      setInterval(this.updateTime, 1000);
    },
  };
  </script>
  
  <style scoped>
  /* Add your component-specific styles here */
  h2 {
    color: #3498db;
  }
  </style>
  