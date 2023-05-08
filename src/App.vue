<template>
 <HeroSection/>
</template>

<script>
import HeroSection from './components/screen/home/HeroSection.vue';

export default {
  name: 'App',
  components: {
    HeroSection,
  },
};
</script>

<style lang="scss">
@import './utils/style/scss/index.scss';
</style>
