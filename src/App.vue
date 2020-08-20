<template>
  <div id="app">
    <div class="w-100 h-100 p-3 mx-auto flex-column">
      <header class="masthead mb-5">
        <div class="inner">
          <h3 class="masthead-brand">Photo Contest</h3>
          <nav class="nav nav-masthead justify-content-center">
            <a class="nav-link active" href="#">Home</a>
            <a class="nav-link" href="#carousel">Carousal</a>
            <a class="nav-link" href="#vote">Vote</a>
          </nav>
        </div>
      </header>
      <div class="col-7 mx-auto">
        <carousel
          id="carousel"
          :perPage="1"
          :navigationEnabled="true"
          :paginationColor="pink"
          :centerMode="true"
          :autoplay="true"
          :loop="true"
        >
          <slide>
            <a href="#con1">
              <img :src="pic[0].src" class="img-fluid" />
            </a>

            <br />
            <br />Contestant No. 1
          </slide>
          <slide>
            <a href="#con2">
              <img :src="pic[1].src" class="img-fluid" />
            </a>

            <br />
            <br />Contestant no.2
          </slide>
          <slide>
            <a href="#con3">
              <img :src="pic[2].src" class="img-fluid" />
            </a>

            <br />
            <br />Contestant no.3
          </slide>
        </carousel>
      </div>
    </div>

    <div id="vote" class="container-fluid">
      <div class="col mx-auto mb-3">
        <h1>Voting</h1>
      </div>

      <div id="con1" class="row align-items-center mb-5">
        <div class="col-md-7">
          <img :src="pic[0].src" class="img-fluid" />
          <br />
          <br />Contestant No. 1
        </div>
        <div class="col-md-5">
          <score />
        </div>
      </div>
      <div id="con2" class="row align-items-center mb-5">
        <div class="col-md-7">
          <img :src="pic[1].src" class="img-fluid" />
          <br />
          <br />Contestant No. 2
        </div>
        <div class="col-md-5">
          <score />
        </div>
      </div>
      <div id="con3" class="row align-items-center mb-5">
        <div class="col-md-7">
          <img :src="pic[2].src" class="img-fluid" />
          <br />
          <br />Contestant No. 3
        </div>
        <div class="col-md-5">
          <score />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "./assets/CSS/cover.css";
import Vue from "vue";
import VueCarousel from "vue-carousel";
Vue.use(VueCarousel);
import score from "./components/score";

export default {
  name: "App",
  components: { score },
  data: function () {
    return {
      pic: [
        {
          src:
            "https://cdn.pixabay.com/photo/2018/01/14/23/12/nature-3082832_960_720.jpg",
        },
        {
          src:
            "https://cdn.pixabay.com/photo/2017/02/08/17/24/butterfly-2049567_960_720.jpg",
        },
        {
          src:
            "https://cdn.pixabay.com/photo/2016/08/11/23/48/italy-1587287_960_720.jpg",
        },
      ],
    };
  },
};
</script>

<style>
</style>
