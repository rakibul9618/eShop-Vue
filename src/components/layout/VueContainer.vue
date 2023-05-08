<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="flex_container" :class="Class && Class">
    <div
      :class="[
        py ? 'container' : 'container padding_0',
        ClassName && ClassName,
      ]"
    >
      <slot></slot>
    </div>
  </div>

  
</template>

<script>
export default {
  name: 'VueContainer',
  props: {
    Class: {
      type: String,
      default: '',
    },
    py: {
      type: Boolean,
      default: true,
    },
    ClassName: {
      type: String,
      default: '',
    },
  },
};
</script>


