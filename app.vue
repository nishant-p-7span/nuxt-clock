<!-- pages/index.vue -->
<template>
  <div>
    <h1>Welcome to My Time App</h1>
    <Clock />
  </div>
</template>

<script>
import Clock from '/components/Clock.vue';

export default {
  components: {
    Clock,
  },
};
</script>

<style>
/* Add your page-specific styles here */
h1 {
  color: #7a34db;
}
</style>
