<template>
  <div class="row">
      <div class="col-8" style="border-style:dotted">
          <div>
              <img class="frame-img" :src="currentImage">
          </div>
      </div>
      <div class="col-4" style="border-style:dotted">
          <img class="frame-btn" id="image1" name="image1" src="@/assets/images/frame1.png" @click="showFrame1()">
          <img class="frame-btn" src="@/assets/images/frame2.png" @click="showFrame2()">
      </div>
  </div>
</template>


<script>
export default {
  name: 'HomePage',
  data() {
      return {
          image1: require("@/assets/images/frame1.png"),
          image2: require("@/assets/images/frame2.png"),
          currentImage: '',
      }
  },
  methods: {
      showFrame1() {
          this.currentImage = this.image1;
      },
      showFrame2() {
          this.currentImage = this.image2;
      }
 
  }
}
</script>

<style>
.frame-btn {
  width: 100px;
  height: 100px;
}

.frame-img {
  width: 500px;
  height: 500px;
}
</style>