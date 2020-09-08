<template>
  <div class="fixed z-50 flex justify-between top-0 left-0 w-full transition-all duration-300" :class="scrollDistHeight<0.75 ? ['bg-transparent', 'absolute'] : ['bg-gray-200', 'shadow-md', 'fixed']" >
    <img v-if="scrollDistHeight<0.75" src="../assets/EMC_logo_white2.png" class="lg:h-24 lg:ml-16  w-auto object-contain" alt="">
    <img v-else src="../assets/EMC_logo_black2.png" class="lg:h-24 lg:ml-16 w-auto object-contain" alt="">
    <div class="flex items-center justify-around font-bold text-lg tracking-wider lg:w-1/3" >
        <p :class="scrollDistHeight<0.75 ?['text-gray-400', 'hover:text-red-600', 'bg-transparent'] : ['text-gray-700', 'hover:text-red-600']" class="cursor-pointer transition font-bold duration-100">Home</p>
        <p :class="scrollDistHeight<0.75 ?['text-gray-400', 'hover:text-red-600', 'bg-transparent'] : ['text-gray-700', 'hover:text-red-600']" class="cursor-pointer transition font-bold duration-100">About</p>
        <p :class="scrollDistHeight<0.75 ?['text-gray-400', 'hover:text-red-600', 'bg-transparent'] : ['text-gray-700', 'hover:text-red-600']" class="cursor-pointer transition font-bold duration-100">Contact</p>
        <p :class="scrollDistHeight<0.75 ?['text-gray-400', 'hover:text-red-600', 'bg-transparent'] : ['text-gray-700', 'hover:text-red-600']" class="cursor-pointer transition font-bold duration-100">Disclaimer</p>
        <p :class="scrollDistHeight<0.75 ?['text-gray-400', 'hover:text-red-600', 'bg-transparent'] : ['text-gray-700', 'hover:text-red-600']" class="cursor-pointer transition font-bold duration-100">Other Work</p>
    </div>
  </div>
</template>

<script>
export default {
    props: ['scrollDist'],
    data() {
        return {
            scrollDistHeight: 0,
        }
    },
    watch: {
        scrollDist() {
            this.scrollDistHeight = this.scrollDist/window.screen.height
        },
    }
}
</script>

<style>
.transition {
    transition-property: all;
}

</style>