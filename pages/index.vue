<template>
  <Head>
    <Title>{{ title }}</Title>
    <Meta name="description" :content="title" />
  </Head>
  <div>
    <NavBar />
    <main
      class="h-[90svh] grid md:grid-cols-1 lg:grid-cols-[1fr_2fr_1fr] items-center bg-slate-300 text-black"
    >
      <aside class="flex flex-col items-end justify-center h-full p-3">
        <h2 id="name" class="text-2xl font-semibold font-libreFranklin">
          {{ name }} - {{ color.toLocaleUpperCase() }}
        </h2>
        <p id="releaseDate" class="text-lg font-heebo">
          Release Date: {{ releaseDate }}
        </p>
        <div id="buttons" class="grid grid-cols-5 gap-2 mt-5 place-items-center justify-normal">
          <button
            v-for="size in shoeSizes"
            :key="size"
            class="w-10 h-10 border border-black rounded-xl"
          >
            {{ size }}
          </button>
        </div>
      </aside>
      <section class="relative flex flex-col items-center justify-center h-full p-12">
        <div>
          <h1 class="text-[20rem] font-libreFranklin font-bold relative z-10 ">
            NIKE
          </h1>
        </div>
        <div
          class="absolute z-20 p-12 rounded-full shadow-2xl shadow-red-600 bg-gradient-to-t from-red-500 to-red-300 top-52"
        >
          <NuxtImg
            src="/assets/shoes.png"
            width="300"
            height="300"
            class="h-full"
          />
        </div>
      </section>
      <aside class="flex flex-col items-start justify-end h-full gap-5 p-3">
        <p id="description">{{ description }}</p>
        <div class="flex flex-row gap-2">
          <button>
            <NuxtImg
              src="/assets/leftArrow.svg"
              width="32"
              class="border-2 border-black rounded-full"
            />
          </button>
          <button>
            <NuxtImg
              src="/assets/rightArrow.svg"
              width="32"
              class="border-2 border-black rounded-full"
            />
          </button>
        </div>
      </aside>
    </main>
  </div>
</template>

<script lang="ts" setup>
const title = ref("Nike | Home");

const name = ref("Jordan 1");
const color = ref("Red");
const releaseDate = ref("10/10/2021");
const shoeSizes = ref([6, 7, 8, 9, 10, 11, 12, 13, 14, 15]);
const description = ref(
  "The Air Jordan 1 Retro High OG 'Bred Toe' showcases a blend of classic color blocking on the iconic silhouette. The shoe's upper combines elements of the 'Bred' and 'Black Toe' colorways, highlighted by a red toe box that replaces the traditional white paneling on the forefoot. The rest of the leather build is finished in black, with contrasting white on the mid-panel, Swoosh, and collar. A Wings logo is stamped on the lateral collar flap, while underfoot, the midsole houses Air in the heel for cushioning."
);
</script>
