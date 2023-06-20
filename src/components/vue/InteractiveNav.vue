<script setup>
import "animate.css";
import { ref } from "vue";
const selectedVal = ref("birth");
const bgResource = {
  birth: {
    url: "/images/birth.jpg",
  },
  presidency: {
    url: "/images/presidency.jpg",
  },
  death: {
    url: "/images/death.jpg",
  },
  legacy: {
    url: "/images/legacy.jpeg",
  },
};
const goTo = (url) => {
  window.location.href = url;
};
</script>

<template>
  <transition name="fade" mode="out-in">
    <div
      class="absolute top-0 left-0 right-0 bottom-0 -z-1 object-cover bg-no-repeat bg-cover"
      :style="`background-image:url(${
        selectedVal != '' ? bgResource[selectedVal].url : ''
      })`"
    ></div>
  </transition>
  <div class="flex flex-wrap gap-8 justify-center items-center z-50">
    <button
      @click="
        goTo('/early-life');
        selectedVal = 'birth';
      "
      type="button"
      class="bg-cover p-8 rounded-xl block max-w-xs text-center text-white text-xl hover:text-3xl shadow transition-all ease-in-out duration-300"
      style="background-image: url(/images/birth.jpg)"
    >
      Birth & Early Life
    </button>
    <button
      @click="
        goTo('/presidency');
        selectedVal = 'presidency';
      "
      type="button"
      class="bg-cover p-8 rounded-xl block max-w-xs text-center text-white text-xl hover:text-3xl shadow transition-all ease-in-out duration-300"
      style="background-image: url(/images/presidency.jpg)"
    >
      Presidency
    </button>
    <button
      @click="
        goTo('/death');
        selectedVal = 'death';
      "
      type="button"
      class="bg-cover p-8 rounded-xl block max-w-xs text-center text-white text-xl hover:text-3xl shadow transition-all ease-in-out duration-300"
      style="background-image: url(/images/death.jpg)"
    >
      Death
    </button>
    <button
      @click="
        goTo('/legacy');
        selectedVal = 'legacy';
      "
      type="button"
      class="bg-cover p-8 rounded-xl block max-w-xs text-center text-white text-xl hover:text-3xl shadow transition-all ease-in-out duration-300"
      style="background-image: url(/images/legacy.jpeg)"
    >
      Legacy
    </button>
  </div>
</template>
