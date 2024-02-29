<script>
import { Swiper, SwiperSlide } from 'swiper/vue'


// Import Swiper styles
import 'swiper/css'

import 'swiper/css/effect-coverflow'
import 'swiper/css/pagination'

// import required modules
import { EffectCoverflow, Pagination, Autoplay } from 'swiper/modules'

export default {
  components: {
    Swiper,
    SwiperSlide
  },
  setup() {
    return {
      modules: [Autoplay, EffectCoverflow, Pagination]
    }
  }
}
</script>

<template>
  <div class="bg">
    <video autoplay muted loop class="video-bg" style="object-fit: cover">
      <source src="" type="video/mp4" />
    </video>
    <div class="content absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2">
      <div class="Ttext">
        <h1>Travel Planer</h1>
        <h2>Make your own Travel!</h2><br><br><br><br><br>
      </div>
      <div class="carousel">
        <swiper
          :effect="'coverflow'"
          :grabCursor="true"
          :centeredSlides="true"
          :slidesPerView="'auto'"
          :coverflowEffect="{
            rotate: 20,
            stretch: 0,
            depth: 150,
            modifier: 1,
            slideShadows: true
          }"
          :loop="true"
          :modules="modules"
          :autoplay="{ delay: 10000 }"
          class="mySwiper"
        >
            <swiper-slide><img src="E:\project\Homep\PlaceImg\france.jpg" /></swiper-slide
          ><swiper-slide><img src="E:\project\Homep\PlaceImg\hmm.png" /></swiper-slide
          ><swiper-slide><img src="E:\project\Homep\PlaceImg\huh.png" /></swiper-slide
          ><swiper-slide><img src="E:\project\Homep\PlaceImg\jerry.jpg" /></swiper-slide
          ><swiper-slide><img src="E:\project\Homep\PlaceImg\rome.jpg" /></swiper-slide
          ><swiper-slide><img src="E:\project\Homep\PlaceImg\venice.jpg" /></swiper-slide>
        </swiper>
      </div>
    </div>
  </div>
</template>

<style scoped>
.bg {
  width: 100%;
  z-index: -1;

}

.video-bg {
  top: 0;
  left: 0;
  width: 100%;
  height: 59.45rem;
  z-index: -2;
  filter: brightness(40%);
}

.content {
  z-index: 1;
  width: 100%;
  height: 90%;
  margin-top: 40px;
}

.Ttext {
  width: 40%;
  height: auto;
  margin-left: 100px;
  margin-top: 100px;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  position: fixed;
}
.Ttext h1{
  font-size: 5.5rem;
  color: white;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
}

.Ttext h2{
  font-size: 2rem;
  color: white;
}
  

.carousel {
  position: relative;
  max-width: 900px;
  height: auto;
  overflow: hidden;
  background-color: rgba(0, 0, 0, 0.25);
  border-radius: 10px;
  position: absolute;
  top: 45%;
  right: 30px;
  transform: translateY(-50%);
  z-index: 1;
  padding: 4px;
  margin-right: 20px;
  backdrop-filter: blur(6px);
  box-shadow: 4px 4px 6px rgba(0, 0, 0, 0.6);
}


#app {
  height: 100%;
}
html,
body {
  position: relative;
  height: 100%;
}

body {
  background: #eee;
  font-family:
    Helvetica Neue,
    Helvetica,
    Arial,
    sans-serif;
  font-size: 14px;
  color: #000;
  margin: 0;
  padding: 0;
  
}

.swiper {
  width: 100%;
  padding-top: 50px;
  padding-bottom: 50px;
}

.swiper-slide {
  background-position: center;
  background-size: cover;
  width: 500px;
  height: 500px;
  border-radius: 20px;
  
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  border-radius: 10px;
  
}

</style>
