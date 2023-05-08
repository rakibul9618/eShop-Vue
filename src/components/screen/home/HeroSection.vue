<template>
  <VueContainer :py="false" class="offers grid col-lg-3 gap-30">
    <div
      v-for="(item, ind) in heroBanner"
      :key="ind"
      class="relative overflow-hidden text-white show_case_item"
    >
      <a href="/">
        <div class="absolute inset-0 banner_image">
          <img
            class="img-cover-center"
            src="{{ item.image }}"
            alt="{{ item.title }}"
          />
        </div>
        <div class="black-layer"></div>
        <div class="relative-up flex flex-col items-start content">
          <h4 :class="ind === 0 ? 'lg_title' : 'sm_title'">{{ item.title }}</h4>
          <p class="mt-1 text-700">{{ item.subtitle }}</p>

          <button v-if="ind === 0" class="mt-2 px-2 py-1 radius-1 white-btn">
            Shop Now
          </button>

          <button v-else class="mt-5 relative">Shop Now</button>
        </div>
      </a>
    </div>
  </VueContainer>
</template>

<script>
import VueContainer from '@/components/layout/VueContainer.vue';

export default {
  name: 'HeroSection',
  components: {
    VueContainer,
  },
  data() {
    return {
      heroBanner: [
        {
          id: 1,
          title: 'Fresh from  the workshops',
          subtitle: 'Pull out all the stops with DIY gifts',
          image: '/images/home-hero-banner.jpg',
          highlight: true,
          href: '/',
        },
        {
          id: 2,
          title: 'New Deals at Best Prices',
          subtitle: 'From $40.00',
          image: '/images/home-banner-01.jpg',
          highlight: true,
          href: '/',
        },
        {
          id: 3,
          title: 'Colorful Redmi  Note 6 Pro',
          subtitle: 'Price just $120.00',
          image: '/images/home-banner-02.jpg',
          highlight: true,
          href: '/',
        },
        {
          id: 4,
          title: '1000 mAh Power Bank',
          subtitle: 'From $40.00',
          image: '/images/home-banner-03.jpg',
          highlight: true,
          href: '/',
        },
      ],
    };
  },
};
</script>
