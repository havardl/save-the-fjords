<template>
<div class="background">
  <div class="title-container">
    <h1>{{title}}</h1>
  </div>
  <div class="tagline-container">
    <template v-for="(tagline,index) in taglines">
      <span class="tagline" :key="index">{{tagline}}</span><br :key="index" />
    </template>
  </div>  
</div>
</template>

<style lang="scss" scoped>
.background { 
 background: transparent url("~static/2_1.jpg") 50% 0 no-repeat fixed; 
 background-size: cover;
 width: 100%;
 min-height: 100vh;
}

h1 {
  font-family: 'Josefin Sans', sans-serif;
  font-size: 500%;
  text-transform: uppercase;
  color: #fff;
  font-weight: 700;
  letter-spacing: 0.2em;
  margin-top: 50px;
}

.tagline-container {
  margin-top: 20%;
}

.tagline {
  text-transform: uppercase;
  color: #000;
  opacity: 1;
  font-family: 'Josefin Sans', sans-serif;
  font-size: 200%;
  font-weight: 400;
  background: #fff;
  padding: 0.4em 0.4em 0.2em 0.4em;
  line-height: 2.5em;  
}
</style>

<script>
export default {
  props: ["title", "taglines"],
  name: "FullpageBackgroundImg"
}
</script>