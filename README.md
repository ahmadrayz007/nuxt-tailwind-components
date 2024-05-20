This repository contains the source code and related files for the Bangoding Nuxt Tailwind Components.

## Author

The Components are maintain by Bangoding

- GitHub: [ahmadrayz007](https://github.com/ahmadrayz007)
- Instagram: [@bangoding.id](https://www.instagram.com/bangoding.id/)

## Table of Contents

- [Bouncy Preload Screen](#bouncy-preload-screen)
- [Support](#support)

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

## Support
If you enjoy my content and would like to support my work, consider buying me a coffee! Your support helps me continue to create and share tips on CSS, Tailwind, Vue.js, and Nuxt.js.

[![Static Badge](https://img.shields.io/badge/Buy%20me%20a%20Ko--fi-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/bangoding)
