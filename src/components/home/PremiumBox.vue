<template>
  <b-col cols="4" class="premuim-box">
    <h1 class="text-left">{{ tourName }}</h1>
    <figure>
      <b-img
        :src="require(`../../assets/${imageUrl}`)"
        fluid
        class="w-100"
      ></b-img>
    </figure>
    <div class="text-right book-now-wrap">
      <div class="start-price">
        starting from
        <div><strong>$180,</strong>00</div>
      </div>
      <book-now>Book Now</book-now>
    </div>
  </b-col>
</template>
<script>
import Button from "../common/Button";
export default {
  name: "PremiumBox",
  props: {
    tourName: String,
    imageUrl: String,
    stratingPrice: String,
    tourUrl: String
  },
  components: {
    "book-now": Button
  }
};
</script>
<style lang="scss">
.premuim-box {
  h1 {
    color: #50473d;
    font-size: 30px;
  }
  figure {
    margin-bottom: 0;
  }
  .book-now-wrap {
    position: relative;
    padding: 5px 30px;
    .start-price {
      color: #000;
      position: absolute;
      text-align: left;
      top: -20px;
      left: 0;
      line-height: 25px;
      strong {
        font-size: 25px;
      }
    }
  }
}
</style>
