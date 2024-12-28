<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Wellcome,</h1>
              <h1 class="text-white">I'm Shahzaib Khan</h1>
              <span class="text-grey">Frontend Web Developer</span><br>
              <v-btn tile dark :style="{ color: '#2E8B57' }" class="mt-8" variant="outlined" href="#contact">
                Contact me
              </v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div style="position: absolute;z-index:999;bottom:0;margin-left: auto;margin-right: auto;left: 0;right: 0;text-align: center;">
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: absolute;z-index: 9999;" class="mt-16">
              <v-img src="shahzaib.png" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="about.png" max-width="300" object-fit="cover"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">About Me</h5>
              <div style="width: 120px;">
                <v-slider v-model="slider2" color="#2E8B57">

                </v-slider>
              </div>
              <h4 class="mt-n4">I am Creative Frontend</h4>
              <h4>Web Developer</h4>
              <p class="text-grey">Self-Motivated Front End Developer spent multiple year's
                learning the curves of Front-end Development from Punjab,
                Pakistan. I am expert in creating responsive, user-friendly
                interfaces and high-performance web applications
                designes to fullfill the demand of the client.</p>
              <br>
              <p class="text-grey">
                Expertise includes variety of frontend tools, i.e. HTML5, css, Tailwind css, Javascript (ES6+), vue.js. My commitment to continuous learning and staying abreast of industry trends enables me to implement cutting-edge solutions that drive business success and deliver exceptional user experiences.
              </p>
              <v-btn tile dark color="#2E8B57" class="mt-4">
                Download Resume
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What I Do</h2>
        <div style="width:120px;margin: 0 auto;">
          <v-slider v-model="slider2" color="#2E8B57" >

          </v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-laptop" color="#2E8B57" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Web Frontend</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Build interactive websites <br />
                  From UI to functionality <br> 
                  I ensure smooth user experience.
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-mobile-alt" color="#2E8B57" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Responsive Web</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Work seamlessly on all devices. <br />
                  Ensuring fluid layouts <br>
                  smooth interactions across screens.
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-camera" color="#2E8B57" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Same as your Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Ideas to life with precision. <br />
                  Everything matches your vision  <br> 
                  Down to the detail.
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#2E8B57" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web Developement</v-btn>
          <v-btn class="mr-2" variant="tonal">From Design</v-btn>
          <v-btn class="mr-2" variant="tonal">From Photographs</v-btn>
          <v-btn variant="tonal">Figma Design Conversion</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12 : 2" :class="{'on-hover' : isHovering}" v-bind="props">
                  <v-img :src="item.img" height="225px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#2E8B57" class="mt-4">Load More</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="software.jpg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>
                  By Shahzaib Khan | 02 Nov 2024
                </v-card-subtitle>
                <v-card-text>
                  We offer tailored creative services that address your unique challenges. Our team specializes in graphic design, branding, and visual storytelling to help bring your ideas to life and engage your audience.
                </v-card-text>
              </v-card>
            </v-col>

            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="developing.jpg" height="200px" cover></v-img>
                <v-card-title>Innovative Solutions for All</v-card-title>
                <v-card-subtitle>
                  By Shahzaib Khan | 02 Nov 2024
                </v-card-subtitle>
                <v-card-text>
                  At InnovateCorp, we strive to bring cutting-edge solutions to your business challenges. Our dedicated team works tirelessly to deliver value through technology, expertise, and unmatched service.
                </v-card-text>
              </v-card>
            </v-col>

            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="young.jpg" height="200px" cover></v-img>
                <v-card-title>Your Growth, Our Priority</v-card-title>
                <v-card-subtitle>
                  By Shahzaib Khan | 12 Nov 2024
                </v-card-subtitle>
                <v-card-text>
                  With a focus on sustainable growth and long-term success, we collaborate with our clients to help them achieve their business goals. Let us be your trusted partner in navigating the complexities of modern markets.
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>

      <v-col cols="12" id="biog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Hire me for your awesome project</h1>
              <p class="text-grey">
                I specialize in crafting custom websites and applications that bring your ideas to life. Let's work together to build something unique and impactful for your business. Get in touch and let's start your project today!
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="#2E8B57" class="mt-15">Hire me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact info.</h1>
              <v-btn icon="fas fa-map-marker-alt" class="mt-10" variant="outlined"></v-btn><br>
              <span class="text-caption">50090 Kharian, Punjab, Pakistan</span><br>
              <v-btn icon="fas fa-phone-alt" class="mt-10" variant="outlined"></v-btn><br>
              <span class="text-caption">00235 -6547</span><br>
              <span class="text-caption">00235 -6547</span><br>
              <v-btn icon="fas fa-envelope" class="mt-10" variant="outlined"></v-btn><br>
              <span class="text-caption">shahzaibk.ch@gmail.com</span><br>
              <span class="text-caption">shahzaib.freelanceofficial@gmail.com</span><br>
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore officiis tempore, soluta voluptatem maiores deserunt illo, ex fuga repellat, sunt impedit omnis iusto atque sapiente animi! Veniam aliquam placeat et!
            </span>
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field label="Name" presistent-hind variant="outlined"></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field label="Phone no" presistent-hind variant="outlined"></v-text-field>
              </v-col>
            </v-row>
            <v-textarea label="Message" presistent-hind variant="outlined"></v-textarea>
            <v-btn color="#2E8B57" class="mt-2">Submit Now</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '../components/NavBar.vue';
import FooterView from '../components/FooterView.vue';

export default defineComponent({
  name: 'HomeView',
  setup() {
    return {
      slider2: 50,

      items: [
        {
          img: "lisbon.png"
        },
        {
          img: "mapty.png"
        },
        {
          img: "omnifood.png"
        },
        {
          img: "natours.png"
        },
        {
          img: "trello.png"
        },
        {
          img: "bakist.png"
        }
      ]
    }
  },

  components: {
     NavBar, FooterView
  },
});
</script>

<style scoped>
  v-container {
    padding: 16px 0;
  }

  .head {
    position: relative;
    text-align: center;
    padding: 12px;
    margin-bottom: 6px;
    height: 400px;
    width: 100%;
    color: white;
  }
  .head:before {
    content: " ";
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 50%;
    background: black;
    transform: skew(0deg, 6deg);
  }
  .head:after {
    content: " ";
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 50%;
    background: black;
    transform: skew(0deg, -6deg);
  }
  .egg {
    display: flex;
    justify-content: center;
    margin-left: 100px;
    margin-top: 50px;
    width: 356px;
    height: 300px;
    background-color: #2E8B57;
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
    overflow: hidden;
  }
  .first {
    width: 100%;
    height: 280px;
    text-align: center;
    padding: 2rem 2rem;
  }
  .child {
    display: inline-block;
    padding: 2rem 1rem;
    vertical-align: middle;
    text-align: center;
    margin-right: 8px;
  }
  .imgHover {
    padding: 0 200px;
  }
  .pre {
    width: 100%;
    height: 470px;
    text-align: center;
    padding: 0 200px;
    background-color: #f5f5f5;
  }
  .hire {
    width: 100%;
    height: 200px;
    padding: 0 200px;
    background-color: #e9e9e9;
    margin-top: -24px;
  }
</style>