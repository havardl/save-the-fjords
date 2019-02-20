<template>
<div class="background">
  <div class="title-container">
    <h1>{{title}}</h1>
  </div>
  <div class="tagline-container">
    <template v-for="(tagline,index) in taglines">
      <span class="tagline" :key="index">{{tagline}}</span><br :key="`br-`+index" />
    </template>
  </div>  
  <span class="photo-accreditation">Photo: <a href="https://www.lukatomac.com/en/gallery/vevring/" target="_blank">Luka Tomac</a></span>
</div>
</template>

<style lang="scss" scoped>
.background { 
  background: transparent url("~static/2_1.jpg") 50% 0 no-repeat fixed; 
  background-size: cover;
  width: 100%;
  min-height: 100vh;
  overflow: hidden;
}

h1 {
  font-family: 'Josefin Sans', sans-serif;
  text-transform: uppercase;
  color: #fff;
  font-weight: 700;
  letter-spacing: 0.2em;
  margin-top: 50px;
}

.tagline-container {
  margin-top: 20%;
}

.photo-accreditation {
  position: absolute;
  right: 5%;
  bottom: 5%;
  color: #fff;
  font-family: 'Josefin Sans', sans-serif;
  font-size: 80%;
  font-weight: 400;
  a {
    color: #fff;
  }
  a:hover {
    text-decoration: none;
  }
}

.tagline {
  text-transform: uppercase;
  color: #000;
  opacity: 1;
  font-family: 'Josefin Sans', sans-serif;
  font-weight: 400;
  background: #fff;
  padding: 0.4em 0.4em 0.2em 0.4em;
  line-height: 2.5em;  
}

@media (max-width: 576px) {
  h1 {
    font-size: 160%!important;
  }  
  .tagline-container {
    position: absolute;
    left: 50%;
    bottom: 15%;
    transform: translate(-50%, 0);
    min-width: 80%;
  }  
  .tagline {
    font-size: 80%;
  }  
  .photo-accreditation {
    font-size: 60%;
    bottom: 3%;
  }  
}

// Small devices (landscape phones, 576px and up)
@media (min-width: 576px) {
  h1 {
    font-size: 150%!important;
  }
  .tagline-container {
    position: absolute;
    left: 50%;
    bottom: 15%;
    transform: translate(-50%, 0);
    min-width: 80%;
  }    
  .tagline {
    font-size: 90%;
  }
}

// Medium devices (tablets, 768px and up)
@media (min-width: 768px) {
  h1 {
    font-size: 300%!important;
  }  
  .tagline-container {
    position: absolute;
    left: 50%;
    bottom: 10%;
    transform: translate(-50%, 0);
    min-width: 80%;
  }    
  .tagline {
    font-size: 180%;
  }
}

// Large devices (desktops, 992px and up)
@media (min-width: 992px) { 
  h1 {
    font-size: 400%!important;
  }  
  .tagline {
    font-size: 200%;
  }  
}

// Extra large devices (large desktops, 1200px and up)
@media (min-width: 1200px) { 
  h1 {
    font-size: 500%!important;
  }    
 }
</style>

<script>
export default {
  props: ["title", "taglines"],
  name: "FullpageBackgroundImg"
}
</script>