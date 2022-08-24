<template>
  <div>
  <nav class="relative flex flex-wrap items-center justify-between px-2 py-3 bg-grey-500 mb-3">
    <div class="container px-4 mx-auto flex flex-wrap items-center justify-between">
      <div class="w-full relative flex justify-between lg:w-auto  px-4 lg:static lg:block lg:justify-start">
        <div>
            <p class="font-bold text-xl text-gray-800">Welcome Admin Gym</p>
            <p class="font-medium text-m text-gray-600">
              24/08/2022
            </p>
          </div>
        <button class="text-black cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none" type="button" v-on:click="toggleNavbar()">
          <i class="fas fa-bars"></i>
        </button>
      </div>
      <div v-bind:class="{'hidden': !showMenu, 'flex': showMenu}" class="lg:flex lg:flex-grow items-center">
        <ul class="flex flex-col lg:flex-row list-none ml-auto">
          <li class="nav-item">
            <a class="px-...ading-lg text-black opacity-75" /><span class="ml-2"></span>
          </li>
          <li class="nav-item">
            <a class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-black hover:opacity-75" href="#pablo">
              <i class="fab fa-twitter text-lg leading-lg text-black opacity-75" /><span class="ml-2"></span>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>
