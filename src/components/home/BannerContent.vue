<template>
    <b-carousel-slide img-blank img-alt="Blank image" class = "banner-carousel">
        <template v-slot:img>
        <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            :src="require(`../../assets/svg/${svg_banner}`)"
            alt="image slot"
        />
        <p class = "banner-text">Book your authentic trip, <br/>get the unique experience.</p>
        <img src = "../../assets/png/booktrip.png" class = "book-trip-svg"/>
        <p class = "book-trip-text"> BOOK A TRIP </p>
        <img src = "../../assets/png/rentcar.png" class = "rent-car-svg" />
        <p class = "rent-car-text"> RENT A CAR </p>
        </template>
    </b-carousel-slide>
</template>

<script>
export default {
    name: "BannerContent",
    props:{
      svg_banner: String
    }
}
</script>
<style>
@font-face {
  font-family: Poppins;
  src: url("../../assets/font/Poppins-Regular.ttf");
}

.banner-text{
  position: absolute;
  left: 8.68%;
  right: 36.39%;
  top: 4.54%;
  bottom: 91.63%;
  font-family: Poppins;
  font-style: normal;
  font-weight: bold;
  font-size: 58px;
  line-height: 87px;
  color: #FFFFFF;
}
.book-trip-text{
  position: absolute;
  left: 11.6%;
  right: 81.53%;
  top: 14.13%;
  bottom: 85.34%;

  font-family: Poppins;
  font-style: normal;
  font-weight: bold;
  font-size: 16px;
  line-height: 24px;
  /* identical to box height */
  color: #FFFFFF;
}
.book-trip-svg{
  position: absolute;
  left: 9.1%;
  right: 89.24%;
  top: 14.24%;
  bottom: 85.49%;


}
.rent-car-text{
  position: absolute;
  left: 23.61%;
  right: 70.21%;
  top: 14.13%;
  bottom: 85.34%;

  font-family: Poppins;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 24px;
  /* identical to box height */
  color: #FFFFFF;
}
.rent-car-svg{
  position: absolute;
  left: 21.11%;
  right: 77.22%;
  top: 14.11%;
  bottom: 85.5%;
}
</style>