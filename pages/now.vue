<template>
  <div class="content-page">
    <Banner height="480px" image="/assets/img/collections/desks/desk0.jpg">
      <div class="text-center">
        <SlideRight :duration="1500" :delay="200">
          <h1 v-if="$store.getters['router/onMountedShow']" class="text-white text-smooth text-shadow">
            <b>Now</b>
          </h1>
        </SlideRight>
        <SlideLeft :duration="1500" :delay="200">
          <h5 v-if="$store.getters['router/onMountedShow']" class="text-white text-smooth text-shadow">
            What am i doing right now ?”
          </h5>
        </SlideLeft>
      </div>
    </Banner>
    <section class="section section-skew">
      <div class="container">
        <Card shadow class="card-content" no-body>
          <div class="px-4 py-5 row justify-content-center">
            <div class="col-lg-9">
              <p>
                <client-only>
                  <md-quote-icon w="14px" h="14px" />
                </client-only>
                At first, i'll be thanking to
                <a href="https://108kb.io/blog/now/">Fariz Rizaldy</a>,
                <a href="https://afrijaldzuhri.wordpress.com/now/">Afrijal Dzuhri</a> and
                <a href="https://www.wahudamon.com/pages/now">Afwa Bagas Wahuda</a>.
                Because all of them, i was inspired to create this page for describing about <b><i>what i'm doing right now</i></b>.
                So, maybe you don't need to ask me frequently about that.
              </p>
              <p>
                If you have your own site, maybe you should to make one, too.
              </p>

              <h2 class="mt-5">
                Careers
              </h2>
              <p>
                <b>Working as a Frontend Engineer at <i>Orami Indonesia</i>.</b>
              </p>

              <h2 class="mt-5">
                Activities
              </h2>
              <ul>
                <li>Learning and research some technology stuff from the internet.</li>
                <li>Coding, reading and blogging for fun.</li>
                <li>Making quality time for my family and girlfriend every weekend. (Umm, from phone maybe ?).</li>
              </ul>

              <h2 class="mt-5">
                My Stacks
              </h2>
              <ul>
                <li>React, Vue or other JavaScript framework for frontend stuff.</li>
                <li>REST or GraphQL for API usage.</li>
                <li>Node with Express for backend services.</li>
                <li>Sometimes using PHP with Laravel or Codeigniter as backend services.</li>
              </ul>

              <h2 class="mt-5">
                Software that i use
              </h2>
              <ul>
                <li>OS: Arch-based Linux</li>
                <li>Code Editor: Visual Studio Code</li>
                <li>Database GUI: DBEaver, PhpMyAdmin and Robo 3T</li>
                <li>Browsers: Google Chrome and Firefox</li>
                <li>Others: GIT Kraken, Spotify, XDMan & Advanced REST Client</li>
              </ul>

              <p class="mt-5">
                <i>Last updated at: December 5, 2019 from Tebet, South Jakarta. Indonesia</i>.
                &nbsp;<a href="https://github.com/sutanlab/sutanlab.id/commits/master/pages/now.vue">History</a>
              </p>
            </div>
          </div>
        </Card>
      </div>
    </section>
  </div>
</template>

<script>
import { SlideXLeftTransition as SlideLeft, SlideXRightTransition as SlideRight } from 'vue2-transitions'
import MdQuoteIcon from 'vue-ionicons/dist/md-quote.vue'
import Card from '~/components/Argon/Card'
import Banner from '~/components/Base/Banner'
import MountedAnimation from '~/mixins/mounted-animation'
import { metaGenerator } from '~/utils/helpers'

export default {
  components: {
    SlideLeft,
    SlideRight,
    Banner,
    Card,
    MdQuoteIcon
  },
  mixins: [MountedAnimation],
  head: () => ({
    title: `Now | ${process.env.AUTHOR}`,
    meta: metaGenerator('article', {
      title: 'Now Page',
      description: `What am i doing right now ? - ${process.env.AUTHOR}`,
      keywords: 'now',
      image: '/icon.png',
      url: '/now'
    })
  })
}
</script>
