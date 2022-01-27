<template>
  <div class="bg-gray-700">
    <div
        class="px-4 py-5 mx-auto sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8"
    >
      <div class="relative flex items-center justify-between">
        <a
            href="/"
            aria-label="Death"
            title="Death"
            class="inline-flex items-center"
        >
          <div class="logo-container">
            <img :src="logo"  alt="logo">
          </div>

          <span
              class="ml-2 text-xl font-bold tracking-wide text-gray-100 uppercase"
          >Death</span
          >
        </a>

        <ul class="flex items-center hidden space-x-8 lg:flex">
          <li>
            <a
                href="/"
                class="inline-flex items-center justify-center h-12 px-6 font-medium tracking-wide text-white transition duration-200 rounded shadow-md bg-deep-purple-accent-400 hover:bg-deep-purple-accent-700 focus:shadow-outline focus:outline-none"
                aria-label="Sign up"
                title="Sign up"
            >
              Agenda tu cita
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>

import logo from "../../assets/img/dead-svgrepo-com.svg"

export default {
  data() {
    return {
      isMenuOpen: false,
      logo
    };
  },
};
</script>

<style>
.logo-container{
  width: 40px;
  height: 40px;
}
</style>