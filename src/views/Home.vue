<template>
  <div class="home">
    <license-form />
  </div>
</template>

<script>
import LicenseForm from "@/components/LicenseForm.vue";

export default {
  name: "home",
  components: {
    LicenseForm
  }
};
</script>

<style lang="scss">
.home {
  width: 100vw;
  height: 100vh;
  display: grid;
  grid-template-columns: auto 800px auto;
  grid-template-rows: 1fr auto 1fr;
  grid-template-areas:
    ". . ."
    ". license ."
    ". . .";
}

.home > * {
  grid-area: license;
}
</style>
