<template>
  <div id="app">
    <headerContent />
    <mainContent msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import styles from './foo.module.css';
import headerContent from './components/header.vue';
import mainContent from './components/main.vue';

export default {
  name: 'App',
  components: {
    mainContent,
    headerContent,
  },
};
</script>

<style>
@import '../public/css/reset.css';
</style>
