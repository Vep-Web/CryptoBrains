<style scoped></style>

<template>
  <div class="teams__container container">
    <h2 class="d-none">About our Consuting Agency Team</h2>
    <div class="teams__left">
      <article>
        <header-block class="teams__descr">
          <slot>About Us</slot>
        </header-block>
        <h2 class="teams__title t-45">About our Consuting Agency Team</h2>
        <span class="teams__info t-18"
          >We create experiences and build products that make business
          grow</span
        >
        <span class="teams__info t-16"
          >Get help from Alex Moore, a professional business coach with advanced
          experience on growth and business scaling.</span
        >
        <div class="teams__block">
          <div class="teams__grade">
            <h3 class="teams__header t-30 star">400+</h3>
            <span class="teams__text t-16">Business Services</span>
          </div>
          <div class="teams__grade">
            <h3 class="teams__header t-30 smile">100+</h3>
            <span class="teams__text t-16">Happy Customer</span>
          </div>
        </div>
      </article>
    </div>
    <div class="teams__right">
      <picture>
        <source srcset="@/img/hero2.webp" type="image/webp" />
        <img src="@/img/hero2.jpg" alt="Decorativ image" />
      </picture>
    </div>
  </div>
</template>

<script>
import headerBlock from "../../../UI/header-block.vue";

export default {
  components: {
    headerBlock,
  },
};
</script>
