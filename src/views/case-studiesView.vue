<style scoped></style>

<template>
  <section class="capital background bac-studies">
    <main-section class="capital__container">
      <template v-slot:name> Case Studies </template>

      <template v-slot:title> Case Studies </template>
    </main-section>
  </section>
  <section class="case">
    <case-photo></case-photo>
  </section>
  <section class="contact" id="contact">
    <contact-component></contact-component>
  </section>
</template>

<script>
import contactComponent from "../components/section/home/contact.vue";
import mainSection from "../UI/main-section.vue";
import casePhoto from "../components/section/case/case.vue";

export default {
  components: {
    contactComponent,
    mainSection,
    casePhoto,
  },
};
</script>
