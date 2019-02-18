<template>
  <section class="container">
    <fullpage-background-img title="Save the Fjords" :taglines="taglines" />
  </section>
  
</template>

<script>
import FullpageBackgroundImg from '~/components/FullpageBackgroundImg.vue'

export default {
  components: {
    FullpageBackgroundImg
  },
  data() {
    return {
      taglines: [
        "Norway's fjords are in danger",
        "You can help"
      ]
    };
  }
}
</script>

<style scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
