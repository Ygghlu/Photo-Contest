<template>
  <div>
    <div class="row ">
      <div class="col-2">
        <button @click="likefunction" class="btn">
          <img class="img-fluid" src="../../public/image/like.png" alt="like" />
        </button>
      </div>
      <div class="col-2">
        <button @click="lovefunction" class="btn">
          <img class="img-fluid" src="../../public/image/love.png" alt="love" />
        </button>
      </div>
      <div class="col-2">
        <button @click="hahafunction" class="btn">
          <img class="img-fluid" src="../../public/image/haha.png" alt="haha" />
        </button>
      </div>
      <div class="col-2">
        <button @click="wowfunction" class="btn">
          <img class="img-fluid" src="../../public/image/wow.png" alt="wow" />
        </button>
      </div>
      <div class="col-2">
        <button @click="sadfunction" class="btn">
          <img class="img-fluid" src="../../public/image/sad.png" alt="sad" />
        </button>
      </div>
      <div class="col-2">
        <button @click="angryfunction" class="btn">
          <img
            class="img-fluid"
            src="../../public/image/angry.png"
            alt="angry"
          />
        </button>
      </div>
    </div>
    <br />
    <p>This photo score : {{ counter }}</p>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      counter: 0,
    };
  },

  methods: {
    likefunction: function() {
      this.counter += 1;
    },
    lovefunction: function() {
      this.counter += 10;
    },
    hahafunction: function() {
      this.counter += 5;
    },
    wowfunction: function() {
      this.counter += 20;
    },
    sadfunction: function() {
      this.counter -= 5;
    },
    angryfunction: function() {
      this.counter -= 50;
    },
  },
};
</script>

<style></style>
