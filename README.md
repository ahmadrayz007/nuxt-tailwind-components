This repository contains the source code and related files for the Bangoding Nuxt Tailwind Components.

## Author

The Components are maintain by Bangoding

- GitHub: [ahmadrayz007](https://github.com/ahmadrayz007)
- Instagram: [@bangoding.id](https://www.instagram.com/bangoding.id/)

## Table of Contents

- [Bouncy Preload Screen](#bouncy-preload-screen)
- [Support](#support)
- [Copy to Clipboard Button](#copy-to-clipboard-button)

## Bouncy Preload Screen
### Requirements

- **Nuxt.js**
- **Tailwind CSS**

```
<template>
  <div class="flex items-center justify-center h-screen">
    <div>
      <div class="inline-flex items-center">
        <div class="relative h-12 w-4">
          <div
            class="absolute inset-0 h-4 w-4 rounded-full bg-[#fbae17] animate-bounce"
          ></div>
        </div>
        <div class="ml-2 text-[#fbae17]">NOW LOADING</div>
      </div>
    </div>
  </div>
</template>

<style>
@keyframes bounce {
  0% {
    top: 1.875rem; /* 30px */
    height: 0.3125rem; /* 5px */
    border-radius: 3.75rem 3.75rem 1.25rem 1.25rem;
    transform: scaleX(2);
  }
  35% {
    height: 0.9375rem; /* 15px */
    border-radius: 50%;
    transform: scaleX(1);
  }
  100% {
    top: 0;
  }
}

.animate-bounce {
  animation: bounce 500ms alternate infinite ease;
}
</style>
```
I got it from this [Codepen](https://codepen.io/wabeshew/pen/XdbBdM) and tranform it into Tailwind and NuxtJs

## Copy to Clipboard Button
### Requirements

- **Nuxt.js**
- **Tailwind CSS**
- Just any icon from svg to an icon pack/library
```
<template>
  <div class="flex items-center">
    <input type="text" v-model="textToCopy" class="hidden" ref="copyText" readonly />
    <button
      @click="copyToClipboard"
      class="flex items-center px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600 focus:outline-none"
    >
      <div v-if="copied">Copied!</div>
      <div v-else>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-5 w-5"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71" />
          <path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71" />
        </svg>
      </div>
    </button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const textToCopy = ref("https://ko-fi.com/bangoding");
const copied = ref(false);

const copyToClipboard = () => {
  navigator.clipboard.writeText(textToCopy.value).then(() => {
    copied.value = true;
  });
};
</script>

<style scoped>
/* You can add any additional styling here if needed */
</style>
```


## Support
If you enjoy my content and would like to support my work, consider buying me a coffee! Your support helps me continue to create and share tips on CSS, Tailwind, Vue.js, and Nuxt.js.

[![Static Badge](https://img.shields.io/badge/Buy%20me%20a%20Ko--fi-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/bangoding)
