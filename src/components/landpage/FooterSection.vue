<template>
  <section id="footer-section">
    <b-container
      fluid
      class="px-5 bg-main-color footer text-white pb-5">
      <b-container>
        <b-row align-h="center">
          <b-col
              sm="6"
              md="6"
              lg="6"
              class="mt-5 pt-lg-0">
              <img src="../../assets/logo-white-new-temp.png"
              class="d-block mx-auto w-50"/>
          </b-col>
        </b-row>
        <b-row>
          <b-col
            lg="6"
            class="h-100 to-be-animated mt-5 list">
            <h5 class="pb-3">Links</h5>
            <hr/>
            <ul>
              <li>
                <a href="https://gitlab.com/cervoneluca/openbits" target="_blank">Green Paper</a>
              </li>
              <li>
                <a href="https://gitlab.com/cervoneluca/openbits-web" target="_blank">Web Site and Web Application Code</a>
              </li>
              <li>
                <a href="https://gitlab.com/cervoneluca/openbits-cli" target="_blank">CLI Code</a>
              </li>
              <li>
                <a href="https://www.npmjs.com/package/openbits" target="_blank">CLI NPM Package</a>
              </li>
            </ul>
          </b-col>
          <b-col
            lg="6"
            class="h-100 to-be-animated mt-5 list  border-left">
            <h5 class="pb-3">Credits</h5>
            <hr/>
            <ul>
              <li>Special thanks to the whole
                <a href="https://www.arweave.org/" target="_blank">Arweave Community</a>!
                They helped a lot in creating OpenBits! Join their discord channel
                <a href="https://discord.gg/q8jxFK" target="_blank">here</a>.
              </li>
              <li data-sourcepos="184:1-184:182">
                The Universe Image in the background is a courtesy of
                <a href="https://www.freepik.com/free-photos-vectors/background" target="_blank">
                  Background vector created by upklyak </a><a href="http://www.freepik.com" target="_blank">
                  www.freepik.com
                </a>.
              </li>
              <li>
                Animated images around the site are derived works of animation downloaded from
                <a href="https://stories.freepik.com/web">Freepik Stories</a>.
              </li>
            </ul>
          </b-col>
        </b-row>
        <b-row>
          <b-col
            lg="12"
            class="h-100 to-be-animated mt-5 list text-center">
            <h6 class="pt-4 copy">
              All the content on this page is distributed under
              the
              <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">
              CC BY-SA 4.0 license</a>.
              All the software that compose OpenBits is distributed
              under the
              <a href="https://opensource.org/licenses/MIT" target="_blank"> MIT license</a>.
              <!-- OpenBits is a property of the MULTIVERSE and was authored by <a
              class="text-white"
              href="mailto:cervoneluca@gmail.com">
              Luca Cervone</a>. -->
            </h6>
          </b-col>
        </b-row>
      </b-container>
    </b-container>
  </section>
</template>

<script>
import config from '@/mixins/configs';

export default {
  name: 'LandPageFooterSection',
  mixins: [config],
};
</script>

<style lang="scss" scoped>
@import '../../assets/styles/custom-theme.scss';

#footer-section {
  .footer {
    min-height:300px;
    h5 {
      border-bottom: 2px solid white;
    }
    .copy{
      border-bottom: none;
      border-top: 2px solid white;
    }
    .border-left{
      border-left: 2px solid white;
    }
    a {
      text-decoration:underline;
      color:white;
    }

  }
}
</style>
