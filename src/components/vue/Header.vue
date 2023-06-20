<script setup>
import { onMounted } from "vue";
onMounted(() => {
  let header = document.getElementById("header");

  document.addEventListener("scroll", function () {
    // Get the scroll position
    if (header) {
      let scrollPos = window.pageYOffset;

      if (scrollPos > 50) {
        header.classList.add("bg-white");
        header.classList.add("text-slate-800");
        header.classList.remove("text-slate-300");
      } else {
        header.classList.remove("bg-white");
        header.classList.add("text-slate-300");
        header.classList.remove("text-slate-800");
      }
    }
  });
});
</script>

<template>
  <div
    id="header"
    class="w-full text-slate-300 fixed top-0 z-50 mx-auto flex flex-row justify-between items-center px-8 py-4 backdrop-filter backdrop-blur-sm bg-opacity-50 shadow-lg transition-all ease-in-out duration-300"
  >
    <div
      class="max-w-7xl mx-auto flex flex-row justify-between items-center w-full"
    >
      <div class="flex items-center gap-2">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="64"
          height="64"
          viewBox="0 0 24 24"
        >
          <path
            class="fill-slate-200"
            fill="currentColor"
            d="M6 18h12V6H6v12Zm8 2h-4v2H8v-2H5a1 1 0 0 1-1-1v-3H2v-2h2v-4H2V8h2V5a1 1 0 0 1 1-1h3V2h2v2h4V2h2v2h3a1 1 0 0 1 1 1v3h2v2h-2v4h2v2h-2v3a1 1 0 0 1-1 1h-3v2h-2v-2ZM8 8h8v8H8V8Z"
          />
        </svg>
        <span class="font-bold text-3xl">Ramon Magsaysay</span>
      </div>
      <div class="flex items-center gap-6">
        <a href="/early-life" class="text-xl">
          <p className=" relative group">
            <span class="group-hover:text-slate-300"
              >The Birth and Early Life</span
            >
            <span
              className="absolute -bottom-1 left-0 w-0 h-1 bg-slate-300 group`-hover:w-full group-hover:transition-all"
            ></span>
          </p>
        </a>
        <a href="/presidency" class="text-xl">
          <p className=" relative group">
            <span class="group-hover:text-slate-300">Presidency</span>
            <span
              className="absolute -bottom-1 left-0 w-0 h-1 bg-slate-300 group-hover:w-full group-hover:transition-all"
            ></span>
          </p>
        </a>
        <a href="/death" class="text-xl">
          <p className=" relative group">
            <span class="group-hover:text-slate-300">Death</span>
            <span
              className="absolute -bottom-1 left-0 w-0 h-1 bg-slate-300 group-hover:w-full group-hover:transition-all"
            ></span>
          </p>
        </a>
        <a href="/legacy" class="text-xl">
          <p className=" relative group">
            <span class="group-hover:text-slate-300">Legacy</span>
            <span
              className="absolute -bottom-1 left-0 w-0 h-1 bg-slate-300 group-hover:w-full group-hover:transition-all"
            ></span>
          </p>
        </a>
      </div>
    </div>
  </div>
</template>
