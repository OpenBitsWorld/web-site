<template>
  <section id="hero-section" class="h-100">
    <b-container
      class="hero h-100 bg-main-color px-3 px-lg-5 px-md-5 px-sm-2"
      fluid>
      <b-row
        class="to-be-animated mt-5 py-3"
        v-animate-onscroll="{down: 'animated fadeInDown'}">
        <b-col
            sm="12"
            md="12"
            lg="12"
            class="pt-lg-0 d-flex align-items-center">
            <img src="../../assets/logo-white-new-temp.png"
            class="mt-5 mx-auto d-block logo"/>
        </b-col>
      </b-row>
      <b-row
        v-animate-onscroll="{down: 'animated fadeInUp'}"
        class="my-5 my-sm-5 my-md-5 my-lg-5 pt-3 to-be-animated">
        <b-col
          sm="12"
          md="12"
          lg="12"
          class="text-center">
          <div
            class="display-4 text-secondary-color section-title
            d-none d-sm-inline-block d-md-inline-block d-lg-inline-block">
            A Rewarding Multiverse For Open Source Packages!
          </div>
          <div
            class="h2 text-secondary-color section-title
            d-inline-block d-sm-none d-md-none d-lg-none">
            A Rewarding Multiverse For Open Source Packages!
          </div>
        </b-col>
      </b-row>
      <b-row
        class="px-3 py-3 text-white text-center"
        cols="3">
        <b-col
          class="big-number-counter-col">
          <font-awesome-icon
            size="3x"
            class="mb-2 mb-sm-2 mb-md-5 mb-lg-5 mx-auto mr-sm-3 mr-md-3 mr-lg-3 d-none d-sm-block
            d-md-inline d-lg-inline"
            icon="box-open" />
          <number
            v-if="openBitsCount"
            ref="numberOfPackages"
            :to="openBitsCount"
            class="text-white display-1 my-5"
            />
          <span
            v-else
            class="text-white display-1 pb-4">
            <LoadingSpinner variant="white" />
          </span>
          <h3 class="d-none d-sm-none d-md-block d-lg-block">Published Packages</h3>
          <h6 class="d-block d-sm-block d-md-none d-lg-none mt-2">Published Packages</h6>
        </b-col>
        <b-col
          class="big-number-counter-col">
          <font-awesome-icon
            size="3x"
            class="mb-2 mb-sm-2 mb-md-5 mb-lg-5 mx-auto mr-sm-3 mr-md-3 mr-lg-3 d-none d-sm-block
            d-md-inline d-lg-inline"
            icon="hand-spock" />
          <number
            v-if="pst"
            ref="numberOfIntstallation"
            :to="parseFloat(pst.generatedProfit).toFixed(2) * 100"
            class="text-white display-1"
            />
          <span
            v-else
            class="text-white display-1 pb-4">
            <LoadingSpinner variant="white" />
          </span>
          <h3 class="d-none d-sm-none d-md-block d-lg-block">Rewarded Installations</h3>
          <h6 class="d-block d-sm-block d-md-none d-lg-none mt-2">Rewarded Installations</h6>
        </b-col>
        <b-col
          class="big-number-counter-col">
          <font-awesome-icon
            size="3x"
            class="mb-2 mb-sm-2 mb-md-5 mb-lg-5 mx-auto mr-sm-3 mr-md-3 mr-lg-3 d-none d-sm-block
            d-md-inline d-lg-inline"
            icon="user-astronaut" />
          <number
            v-if="pst"
            ref="numberOfIntstallation"
            :to="Object.keys(pst.users).length"
            class="text-white display-1"
            />
          <span
            v-else
            class="text-white display-1 pb-4">
            <LoadingSpinner variant="white" />
          </span>
          <h3 class="d-none d-sm-none d-md-block d-lg-block">Unique Users</h3>
          <h6 class="d-block d-sm-block d-md-none d-lg-none mt-2">Unique Users</h6>
        </b-col>
      </b-row>
      <b-row
        v-animate-onscroll="{down: 'animated fadeInUp'}"
        class="mt-2 mt-sm-2 mt-md-5 mt-lg-5 to-be-animated px-2 text-center">
        <b-col
          cols="12"
          class="d-none d-sm-none d-md-inline-block d-lg-inline-block">
          <b-button
            size="lg"
            variant="multiverse-color"
            class="mr-2"
            href="/#/explore-openbits" target="_blank">
              <b>Explore All OpenBits</b>
          </b-button>
          <b-button
            v-scroll-to="'#why-section'"
            class="ml-md-3 ml-lg-3 mt-2 mt-sm-0 mt-md-0 mt-lg-0 mr-md-3 mr-lg-3"
            size="lg"
            variant="outline-multiverse-color text-white">Learn More On OpenBits</b-button>
        </b-col>
        <b-col
          cols="12"
          class="d-inline-block d-sm-inline-block d-md-none d-lg-none">
          <b-button
            variant="multiverse-color"
            href="/#/explore-openbits" target="_blank">
              <b>Explore All OpenBits</b>
          </b-button>
          <b-button
            v-scroll-to="'#why-section'"
            class="mt-1 d-block mx-auto"
            variant="outline-multiverse-color text-white">Learn More On OpenBits</b-button>
        </b-col>
      </b-row>
    </b-container>
    <svg class="hero-waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 24 150 28 " preserveAspectRatio="none">
      <defs>
        <path id="wave-path" d="M-160 44c30 0 58-18 88-18s 58
        18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
      </defs>
      <g class="wave1">
        <use xlink:href="#wave-path" x="50" y="3" fill="rgba(255,255,255, .1)" />
      </g>
      <g class="wave2">
        <use xlink:href="#wave-path" x="50" y="0" fill="rgba(255,255,255, .2)" />
      </g>
      <g class="wave3">
        <use xlink:href="#wave-path" x="50" y="9" fill="#fff" />
      </g>
    </svg>
  </section>
</template>

<script>
import Vue from 'vue';
import { readContract } from 'smartweave';
import config from '@/mixins/configs';
import LoadingSpinner from '@/components/LoadingSpinner.vue';

export default {
  name: 'LandPageHeroSection',
  mixins: [config],
  components: {
    LoadingSpinner,
  },
  async mounted() {
    window.scroll(0, 1);
    this.countOpenBits();
    this.pstStatus();
  },
  methods: {
    async pstStatus() {
      // get the openbits PST Status
      const OpenBitsPSTStatus = await readContract(
        Vue.$arweave.node,
        this.config.OPENBITS_CBVAC_STATUS,
      );
      this.pst = OpenBitsPSTStatus;
    },
    async countOpenBits() {
      // get openbits from the registry
      const rs = await readContract(Vue.$arweave.node, this.config.OPENBITS_REGISTRY);
      // get the openbits
      const { OpenBits } = rs;
      Object.values(OpenBits.nodePackages).forEach((v) => {
        if (v.name !== '@theronin/solarweave') {
          this.openBitsCount += 1;
        }
      });
    },
  },
  data() {
    return {
      pst: null,
      openBitsCount: 0,
    };
  },
};
</script>

<style lang="scss" scoped>
@import '../../assets/styles/custom-theme.scss';

#hero-section{
  margin-top:-120px;
  .hero {
    background: url("../../assets/multiverse-wallpaper.jpg");
    background-repeat:no-repeat;
    position: relative;
    padding: 7rem 0 0 0;
    background-size: auto 100%;
    .to-be-animated {
      transition-duration: 800ms;
      &:not(.animated) {
        opacity: 0;
      }
    }
    &:before {
      content: "";
      background-color:transparentize(black, 0.30);
      position: absolute;
      bottom: 0;
      top: 0;
      left: 0;
      right: 0;
    }
    .logo{
      display:block;
      width:29rem;
      @media (max-width: 767px) {
        width:20rem;
      }
    }
    .hero-screenshot {
      width:100%;
    }
    h1 {
      margin: 0 0 20px 0;
      font-size: 4em;
      font-weight: 700;
      line-height: 56px;
    }
    h2 {
      margin-bottom: 40px;
      font-size: 2em;
      span {
        border-bottom: 4px solid white;
      }
    }
  }
  .hero-waves{
    margin-top:-406px;
  }
  .hero-waves {
    display: block;
    margin-top: -60px;
    width: 100%;
    height: 60px;
    z-index: 5;
    position: relative;
  }
  .wave1 use {
    -webkit-animation: move-forever1 10s linear infinite;
    animation: move-forever1 10s linear infinite;
    -webkit-animation-delay: -2s;
    animation-delay: -2s;
  }
  .wave2 use {
    -webkit-animation: move-forever2 8s linear infinite;
    animation: move-forever2 8s linear infinite;
    -webkit-animation-delay: -2s;
    animation-delay: -2s;
  }
  .wave3 use {
    -webkit-animation: move-forever3 6s linear infinite;
    animation: move-forever3 6s linear infinite;
    -webkit-animation-delay: -2s;
    animation-delay: -2s;
  }
  @-webkit-keyframes move-forever1 {
    0% {
      transform: translate(85px, 0%);
    }
    100% {
      transform: translate(-90px, 0%);
    }
  }
  @keyframes move-forever1 {
    0% {
      transform: translate(85px, 0%);
    }
    100% {
      transform: translate(-90px, 0%);
    }
  }
  @-webkit-keyframes move-forever2 {
    0% {
      transform: translate(-90px, 0%);
    }
    100% {
      transform: translate(85px, 0%);
    }
  }
  @keyframes move-forever2 {
    0% {
      transform: translate(-90px, 0%);
    }
    100% {
      transform: translate(85px, 0%);
    }
  }
  @-webkit-keyframes move-forever3 {
    0% {
      transform: translate(-90px, 0%);
    }
    100% {
      transform: translate(85px, 0%);
    }
  }
  @keyframes move-forever3 {
    0% {
      transform: translate(-90px, 0%);
    }
    100% {
      transform: translate(85px, 0%);
    }
  }
}
</style>
