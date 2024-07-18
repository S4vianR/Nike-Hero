<template>
  <div>
    <nav
      class="p-3 h-[10svh] flex flex-row justify-evenly items-center"
    >
      <NuxtImg
        src="/assets/logo.png"
        alt="Nike Logo"
        class="h-16"
      />
      <ul class="flex flex-row gap-24 font-semibold font-oswald">
        <li>
          <a href="#"> NEW RELEASE </a>
        </li>
        <li>
          <a href="#"> MEN </a>
        </li>
        <li>
          <a href="#"> WOMEN </a>
        </li>
        <li>
          <a href="#"> KIDS </a>
        </li>
        <li>
          <a href="#"> CUSTOMIZE </a>
        </li>
      </ul>
      <div class="flex flex-row items-center justify-center gap-3">
        <button>
          <NuxtImg src="/assets/userIcon.svg" alt="User Icon" class="w-6" />
        </button>
        <button>
          <NuxtImg src="/assets/cartIcon.svg" alt="Shopping Bag" class="w-6 "/>
        </button>
      </div>
    </nav>
  </div>
</template>