<template>
<div class="home-page grid-container full">
  <header-section></header-section>
  <hero-section></hero-section>
  <footer-section></footer-section>
</div>
</template>

<script>
import HeaderSection from '@/components/HeaderSection';
import HeroSection from '@/components/HeroSection';
import FooterSection from '@/components/FooterSection';

const HomePage = {
  name: 'home-page',
  components: {
    HeaderSection,
    HeroSection,
    FooterSection,
  },
};

export default HomePage;
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
$gray: #808080;
$highlight: #4ec6cd;
$nav-text-color: $gray;
$vert-seperate: 4rem;

.home-page_body {

  /* Small only */
  @media screen and (max-width: 39.9375em) {
    margin: 60px 0 30px;
  }
}

.block {
  position: relative;
  height: 100%;
  width: 100%;
  max-height: 250px;
  overflow: hidden;
  border: 1px solid white;
  background: black;
  opacity: 0.8;
  transition: opacity 0.2s ease-out;
  cursor: pointer;

  &:hover {
    transition: opacity 0.2s ease-in;
    opacity: 1;

  }
}

.b1 {
  grid-area: big-top;

}

.b2 {
  grid-area :small-top;
}

.b3 {
  grid-area: small-middle;
}

.b4 {
  grid-area: big-middle;
}

.footer {
  position:fixed;

  /* Small only */
  @media screen and (max-width: 39.9375em), (max-height: 720px) {
    position: relative;
  }
}
</style>
