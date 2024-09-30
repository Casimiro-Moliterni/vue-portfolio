<script>
import { ImgComparisonSlider } from "@img-comparison-slider/vue";
export default {
  name: "Projects",
  components: {
    ImgComparisonSlider,
  },
};
</script>

<template>
  <section class="border">
    <div class="container">
      <h1>Sezione Progetti</h1>
      <img-comparison-slider hover="hover" value="50">
        <img
          slot="first"
          width="100%"
          src="../assets/img/io-2.png"
        />
        <img
          slot="second"
          width="100%"
          src="../assets/img/io.jpg"
        />
      </img-comparison-slider>
    </div>
  </section>
</template>

<style  type="text/css">
 img-comparison-slider{
    --divider-width: 2px;
    --divider-color: #c0c0c000;
    --default-handle-opacity: 0.3;
    --default-handle-opacity:0
}
img-comparison-slider:hover{
      --exposure:10%

  }
</style>
