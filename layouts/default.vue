<template>
  <div class="twoColHybLtHdr">
    <div id="container">
      <main-header/>
      <side-bar/>
      <nuxt/>
      <site-footer/>
    </div>
  </div>
</template>

<script>
import MainHeader from '~/components/old/MainHeader.vue';
import SideBar from '~/components/old/SideBar.vue';
import SiteFooter from '~/components/old/SiteFooter.vue';
export default {
  components: { MainHeader, SideBar, SiteFooter }
};
</script>

<style>
@charset "utf-8";
body {
  font: 100% Verdana, Arial, Helvetica, sans-serif;
  margin: 0;
  padding: 0;
  text-align: center;
  color: #000000;
  background-color: #d4d3d2;
}
h1 {
  letter-spacing: 0.2em;
  font-family: Georgia, 'Times New Roman', Times, 'serif medium';
  text-transform: uppercase;
  color: #d1570d;
  font-size: medium;
}

.twoColHybLtHdr #container {
  width: 80%;
  margin: 0 auto;
  border: 0px none #000000;
  text-align: left;
}
.twoColHybLtHdr #header {
  height: 120px;
  padding: 0 10px 0 100px;
  background-color: #d1570c;
  background-repeat: no-repeat;
  margin-bottom: 20px;
  background-image: url(/images/half-black-half-white-butterfly.jpg);
  border: medium solid #535353;
}
.twoColHybLtHdr #header h1 {
  margin: 0;
  padding-right: 0;
  padding-left: 0;
  padding-bottom: 10px;
}

.twoColHybLtHdr #sidebar1 {
  float: left;
  width: 10em;
  padding: 15px 0;
  overflow: visible;
  border-radius: 6px;
}
.twoColHybLtHdr #sidebar1 h3,
.twoColHybLtHdr #sidebar1 p {
  margin-left: 10px;
  margin-right: 10px;
}

.twoColHybLtHdr #mainContent {
  background-position: top;
  top: auto;
  position: relative;
  bottom: auto;

  padding: 5px;
  margin-right: 20px;
  margin-bottom: 0;
  margin-left: 12em;
  border-radius: 6px;
}
.twoColHybLtHdr #footer {
  padding: 0 10px;
  position: relative;
}
.twoColHybLtHdr #footer p {
  margin: 0;
  padding: 10px 0;
}
.twoColHybLtHdr #mainContent #cook {
  border-style: dotted;
  background: #d1570d;
  margin: 5px 45px;
  padding: 5px;
}

.fltrt {
  float: right;
  margin-left: 8px;
  padding-top: 10px;
  padding-bottom: 10px;
}
.fltlft {
  float: left;
  margin-right: 8px;
}
.clearfloat {
  clear: both;
  height: 0;
  font-size: 1px;
  line-height: 0px;
}

#sidebar1 .paypal {
  text-align: center;
}
.photos {
  text-align: center;
}
.photos img {
  padding-right: 10px;
  padding-left: 10px;
}
.center {
  text-align: center;
}

.box {
  border: medium solid #000;
  padding: 5px;
}
.style1 {
  color: #ff9900;
  font-size: x-large;
  font-style: italic;
}
.style3 {
  font-size: 14px;
}
.style4 {
  color: #fde792;
}
.style5 {
  font-family: 'Times New Roman', Times, serif;
}
.style6 {
  font-size: small;
  font-family: 'Times New Roman', Times, serif;
}
</style>
