<template>
  <div style="font-family: Rajdhani; background: #1b1b1b;" class="flex flex-col w-full relative  overflow-x-hidden"> 
      <Navbar :scrollDist="scrollDist" />


      <div class="overflow-hidden full h-screen relative flex justify-center overflow-x-hidden" style="pointer-events:none">
        <div class="absolute z-20 h-full w-full flex flex-col justify-end">
          <p style="pointer-events: auto" class="text-white cursor-pointer hover:underline text-2xl">Scroll down to see more</p>
        </div>
        <div class="absolute z-20 w-full h-full flex items-center justify-center container">
            <iframe class="fade-in slide-in from-left" style="pointer-events:auto" width="560" height="315" src="https://www.youtube.com/embed/1B42ofpOQTc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="flex-1 fade-in slide-in from-right flex flex-col text-white items-center">
              <p class="tracking-widest font-bold text-gray-100 text-sm uppercase">New release</p>
              <p class="text-5xl ">Chapter 7 </p>
              <p class="text-5xl border-t mb-6">STEMI Equivalents <br></p>
              <p class="text-2xl fade-in slide-in from-right text-left w-1/2 mb-2">Patterns covered:</p>
              <div class="flex fade-in slide-in from-right w-1/2">
                <div class="flex flex-col text-lg items-start">
                  <li>LBBB+Sgarbossa</li>
                  <li>RBBB+LAFB</li>
                  <li>Subtle LAD Occlusion</li>
                  <li>De Winters T waves </li>
                </div>
                <div class="flex flex-col text-lg items-start ml-8">
                  <li>High Lateral MI</li>
                  <li>Subtle Inferior</li>
                  <li>aVR elevation</li>
                  <li>​Posterior MI</li>
                </div>
              </div>
            </div>
        </div>
        <img class="object-cover w-full h-auto " :style="{transform: 'translateY('+scrollDist*0.6+'px)'}" style="filter: brightness(50%);" src="../assets/NYC.png" alt="">
      </div>

      <div class="flex justify-center" style="background: #1b1b1b">
        <div class="container flex justify-around pt-24 pb-12">
          <div class="flex flex-col">
            <p class="text-white border-t-2 pr-16 text-xl tracking-widest uppercase pt-2 border-white">Episodes</p>
          </div>
          <a href="https://www.youtube.com/watch?v=jrAo_ntDfZ8" target="_blank" class="fade-in slide-in from-bottom h-64 flex text-gray-300 hover:bg-gray-900 hover:shadow-lg cursor-pointer p-2 hover:text-white transition duration-200 ease-in-out">
            <div class="h-full w-64 bg-white ">
              <img src="https://i.ytimg.com/vi/jrAo_ntDfZ8/hqdefault.jpg" class="h-full w-auto object-cover"  alt="">
            </div>
            <div class="flex flex-col fade-in slide-in from-bottom  items-start justify-center pl-4">
              <p class="text-4xl">Ep. 6: Ketamine</p>
              <p class="border p-2 px-6 text-red-500 border-red-500 font-bold text-lg">YouTube</p>
            </div>
          </a>
          <div href="https://www.youtube.com/watch?v=_UpT3dVnWMY" target="_blank" class="fade-in slide-in from-bottom h-64 flex text-gray-300 hover:bg-gray-900 hover:shadow-lg cursor-pointer p-2 hover:text-white transition duration-200 ease-in-out">
            <div class="h-full w-64 bg-white ">
              <img src="https://i.ytimg.com/vi/_UpT3dVnWMY/hqdefault.jpg" class="h-full w-auto object-cover"  alt="">

            </div>
            <div class="flex flex-col fade-in slide-in from-bottom  items-start justify-center pl-4">
              <p class="text-4xl">Taming The Tiger</p>
              <p class="border p-2 px-6 text-orange-500 border-orange-500 font-bold text-lg">SoundCloud</p>
            </div>
          </div>
        </div>
      </div>
      <div class="w-full justify-center flex pb-24" style="background: #1b1b1b">
        <div class="container flex pl-auto items-center">
          <div class="bg-gray-700 w-48 h-1 mr-4 ml-auto" style="height: 2px;"></div>
          <p class="text-gray-400 cursor-pointer hover:text-white text-2xl font-bold">VIEW ALL</p>
        </div>
      </div>

      <div class="flex justify-center my-24 rounded-md" style="background: #1b1b1b; height: 60vh;">
        <div class="container flex" style="background: #262626">
          <div class="w-2/3 flex flex-col items-start p-4 text-white text-xl">
            <p class="uppercase text-2xl font-bold mb-2">Episode 1: Cardiac Tamponade Lyrics</p>
            
            <p>[Intro]</p>
            <p>EMC, chapter 1</p>
            <p>See, diagnosing tamponade doesn't take an act of god</p>
            <p  class="">Just a few easy steps makes you the man for the job</p>
            <div class="py-3"></div>
            <p @click="selected=(selected==1 ? 0 : 1)" class="bg-gray-800 hover:bg-gray-700 cursor-pointer transition duration-200">Step 1: Parasternal long, find the effusion</p>
            <div @click="selected=(selected==2 ? 0 : 2)" class="flex flex-col hover:bg-gray-700 bg-gray-800">
              <p class="cursor-pointer text-left transition duration-200">Step 2: The IVC, when they breath what's it doing?</p>
              <p class="cursor-pointer text-left transition duration-200">If the fluid is backing up, won't be flattening or relaxing</p>
              <p class="cursor-pointer text-left transition duration-200">The walls remain static</p>
              <p class="cursor-pointer text-left transition duration-200">Even the fatness of the hepatic vein can be dramatic</p>
            </div>
            
            <div class="py-3"></div>
            <p class="">Step 3: The RV free wall you should be asking,</p>
            <p class="">Is it actually collapsing when it should be expanding?</p>
            <div class="py-6"></div>
            <p class="cursor-pointer transition duration-200">To be continued?</p>




          </div>
          <div class="flex-1 p-2 px-4 flex items-stretch flex-col">
            <p class="uppercase text-2xl font-bold mb-2 text-white">Notes from EMC</p>
            <div v-if="selected==1" class="bg-white  py-3 rounded-md px-4 text-left text-black text-xl font-bold" >
              <p>Comment #1: <br>  Something about the PSTL, could include an image here!</p>
              <img src="https://images.squarespace-cdn.com/content/v1/5c69e7d7b91449698da66e65/1563999623406-JSX2NM93M0SCHB5QQE8B/ke17ZwdGBToddI8pDm48kNrEoSaZaGEx37ScrnN1QRtZw-zPPgdn4jUwVcJE1ZvWEtT5uBSRWt4vQZAgTJucoTqqXjS3CfNDSuuf31e0tVFp0eJd0Vvy0y2OYJX6hH-R4RVCGj_n7XTFnHE0A4DGIu87Nsj43NRAr6WuWZv5DKs/ezgifTamponade.gif" alt=""> 
          </div>
            <div v-if="selected==2" class="bg-white py-3 rounded-md px-4 text-left text-black text-xl font-bold" >
              <p>Comment #2: <br>  Something about the IVC, could include an image here!</p>
              <img src="https://thumbs.gfycat.com/UnsteadyFelineAmericanbittern-size_restricted.gif" alt=""> </div>
          </div>
        </div>
      </div>

      <div class="flex justify-center relative py-32" style="background: #262626; height: 50vh">
        <div class="absolute opacity-50 top-0 h-full" style="left: 10%;">
          <img class="h-full z-50" src="http://nebula.wsimg.com/e47b3e26c224ee390bf76983e04cc645?AccessKeyId=01888D897596FC7CAA61&disposition=0&alloworigin=1" alt="">
        </div>
        <div class="w-1/3"></div>
        <div class="w-2/3 flex fade-in slide-in from-right flex-col items-start justify-center">
          <h1 class="text-white text-4xl font-bold">About</h1>
          <h1 class="text-white text-2xl w-3/4 text-left">This site is a work in progress, and its content is the work of Christopher Hahn, a physician in Emergency Medicine with a special interest in ED flow. In creating the EMC, he has combined his passions of music and medicine with the goal of entertaining and educating students and medical professionals about topics in Emergency Medicine. The ambitious goal will be to post new material monthly. Suggestions for content are welcome. The site also will aim to use hip-hop music as an instrument to inform and reach out to the general public about public health issues that affect us all. </h1>
        </div>
      </div>
      
      <div class="flex justify-center" style="background: #1b1b1b">
        <div class="container flex flex-row-reverse justify-around pt-32 pb-12">
          <div class="flex flex-col">
            <p class="text-white border-t-2 pl-16 text-xl tracking-widest uppercase pt-2 border-white">Just for Fun</p>
          </div>
          <a href="https://www.youtube.com/watch?v=jrAo_ntDfZ8" target="_blank" class="fade-in slide-in from-bottom h-64 flex flex-row-reverse text-gray-300 hover:bg-gray-900 hover:shadow-lg cursor-pointer p-2 hover:text-white transition duration-200 ease-in-out">
            <div class="h-full w-64 bg-white ">
              <img src="https://i.ytimg.com/vi/QJ5VuX8Cm9Y/hqdefault.jpg" class="h-full w-auto object-cover"  alt="">
            </div>
            <div class="flex flex-col fade-in slide-in from-bottom  items-start justify-center pr-4">
              <p class="text-4xl">Triple Scan</p>
              <p class="border p-2 px-6 text-red-500 border-red-500 font-bold text-lg">YouTube</p>
            </div>
          </a>
          <div href="https://www.youtube.com/watch?v=_UpT3dVnWMY" target="_blank" class="fade-in slide-in from-bottom h-64 flex flex-row-reverse text-gray-300 hover:bg-gray-900 hover:shadow-lg cursor-pointer p-2 hover:text-white transition duration-200 ease-in-out">
            <div class="h-full w-64 bg-white ">
              <img src="https://i.ytimg.com/vi/0YHu42o7DSs/hqdefault.jpg" class="h-full w-auto object-cover"  alt="">

            </div>
            <div class="flex flex-col fade-in slide-in from-bottom  items-start justify-center pr-4">
              <p class="text-4xl text-left">Highland EM <br> recruiting</p>
              <p class="border p-2 px-6 text-red-500 border-red-500 font-bold text-lg">YouTube</p>
            </div>
          </div>
        </div>
      </div>
      <div class="w-full justify-center flex flex-row-reverse pb-32" style="background: #1b1b1b">
        <div class="container flex pl-auto items-center">
          <p class="text-gray-400 cursor-pointer  hover:text-white text-2xl font-bold">VIEW ALL</p>
          <div class="bg-gray-600 w-48 h-1 ml-4 mr-auto" style="height: 2px;"></div>
        </div>
      </div>
      
      <Foot/>

  </div>
</template>

<script>
import Foot from "../components/Foot.vue"
import Navbar from "../components/Navbar.vue"

export default {
  name: 'Home',
  components: {
    Foot,
    Navbar
  },
  methods: {
    updateScroll() {
      this.scrollDist = window.scrollY
    }
  },
  data() {
    return {
     scrollDist: 0,
     faders: undefined,
     selected: 0,
    }
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll);
    this.faders = document.querySelectorAll('.fade-in')
    this.sliders = document.querySelectorAll('.slide-in')
    const appearOptions = {
      threshold: 0,
      rootMargin: "0px 0px -100px 0px"
    };
    let appearOnScroll = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(!entry.isIntersecting) {
          return; 
        } else {
          entry.target.classList.add('appear');
          appearOnScroll.unobserve(entry.target)
        }
      })
    }, appearOptions);
    this.faders.forEach(fader => {
      appearOnScroll.observe(fader)
    })
    this.slider.forEach(slider => {
      appearOnScroll.observe(slider)
    })
  }
}
</script>


<style>
.fade-in {
  opacity: 0;
  transition: opacity 250ms ease-in; 
}

.fade-in.appear {
  opacity: 1;
}

.from-left {
  transform: translateX(-10%);
} 

.from-right {
  transform: translateX(10%);
}

.from-left,
.from-right{
  opacity: 0;
  transition: opacity 850ms ease-in, transform 1000ms ease-in;
}
.from-left.appear,
.from-right.appear {
  transform: translateX(0%);
  opacity: 1;
}

.from-bottom {
  transform: translateY(10%);
} 

.from-top {
  transform: translateY(-10%);
}

.from-bottom,
.from-top{
  opacity: 0;
  transition: opacity 850ms ease-in, transform 1000ms ease-in;
}
.from-bottom.appear,
.from-top.appear {
  transform: translateY(0%);
  opacity: 1;
}
</style>