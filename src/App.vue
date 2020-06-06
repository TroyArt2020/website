<template lang="pug">
#app
  header(class="bg-gray-200 bg-cover bg-center" :style="`background-image: url('${images.random().url}.jpg');`")
    .overlay(class="bg-black bg-opacity-50 text-white h-full p-6 flex flex-col items-center justify-center")
      .copy(class="mb-6 text-6xl font-bold text-center") Troy Art Group
      .buttons(class="flex mb-6")
        a(class="btn btn-blue text-white text-center shadow-xl mr-3" href="#") Visit on Facebook
        a(class="btn btn-green text-white text-center shadow-xl" href="#") Donate with Venmo
      .notice(class="text-sm text-center px-10") All donations go directly towards artists & supplies.
  main(class="p-6")
    .notice(class="bg-gray-300 text-sm border border-gray-600 p-3 mb-6")
      div(class="mb-2") Some works are in progress. If you would like to be attributed to any of these works please, contact us on Facebook and we will add proper attribution for you.
      div Click the thumbnails for the full sized image.
    Gallery(:images="images")
</template>

<script>
import Gallery from './components/Gallery.vue'

Array.prototype.random = function () {
  return this[Math.floor((Math.random()*this.length))];
}

export default {
  name: 'App',
  components: { Gallery },
  data: function() {
    return {
      images: [
        { url: 'https://imgur.com/HZxf94z', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/XEYxeqE', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/rNfX1XI', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/rzzv6mq', attributions: ['@dipsoulion'], date: '2020-06-05' },
        { url: 'https://imgur.com/JHDqoQ5', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/2muzBMW', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/ldxGBFh', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/0pTJlgS', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/aXHx1Og', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/a1eKBsg', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/35x7nAW', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/lLFekDl', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/PuKTzad', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/weT93oj', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/wx4MtUl', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/UmOW2GI', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/dt1zuP2', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/angu5xC', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/RwuAUF4', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/Lnm3YRT', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/L40DBsv', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/lWXX8PN', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/BrI8jsg', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/4Ec6oYe', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/FaHDBU5', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/Eujb0CV', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/TFfMch3', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/FQ35zF1', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/k4fe7eM', attributions: ['ZK'], date: '2020-06-05' },
        { url: 'https://imgur.com/ovYTE5k', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/aonKaUD', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/9T4dSzX', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/DuHkH9L', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/5SrScMx', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/MqFWaeb', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/LfePEOK', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/WrhpxqX', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/tA9sGxV', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/fNC5RuY', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/6KccWBZ', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/pgErLOm', attributions: ['@paintedpea', '@dipsoulion'], date: '2020-06-05' },
        { url: 'https://imgur.com/OB8X9o0', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/ZnW8GFQ', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/ZNYTt2Y', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/LUAI27i', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/dBaLApl', attributions: ['JMR'], date: '2020-06-05' },
        { url: 'https://imgur.com/KJyrU1x', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/XAFGBxX', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/zcDoURr', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/bJVZHyX', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/2PxcDKQ', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/kAOEiWb', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/wBFugbV', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/fku7adZ', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/P3g3u86', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/uphpgb3', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/P56fBtH', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/2hzm5Ea', attributions: ['@therealcutz', '@wheredidswaygo', 'ZK'], date: '2020-06-05' },
        { url: 'https://imgur.com/R4B3g2r', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/4UKGOyD', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/rJSk2Is', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/K8DVEB6', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/uU0cCbS', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/zp8aUi4', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/xHQoWH5', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/xpRq7rX', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/l2n28GT', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/DEMFHeg', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/S9lt0rF', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/NdtcZ9i', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/uHZAYZd', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/drQSvj8', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/agUFHCE', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/cQ4guNc', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/tlUcqNQ', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/o6TFuX5', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/llvr17Y', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/uWjZpte', attributions: ['Kriztix'], date: '2020-06-05' },
        { url: 'https://imgur.com/veC5rMC', attributions: [], date: '2020-06-05' },
        { url: 'https://imgur.com/bmJMIW0', attributions: ['S. Kowalewski'], date: '2020-06-05' },
        { url: 'https://imgur.com/O6IvFTA', attributions: [], date: '2020-06-05' },
      ],
    };
  },
}
</script>

<style>
html { @apply leading-none; }

input, select, button {
  @apply text-gray-900 bg-gray-100 py-2 px-3;

  &:focus { @apply shadow-outline; }
  &:disabled { @apply bg-gray-400 text-gray-700 cursor-not-allowed; }
  &::placeholder { @apply text-gray-700; }
}

input, button { @apply appearance-none; }

/* Style with text-*, bg-*, etc. */
.btn { @apply font-bold flex items-center justify-center py-2 px-4 select-none; }
.btn-green {
  @apply bg-green-700;

  &:hover { @apply bg-green-600; }
}
.btn-red {
  @apply bg-red-700;

  &:hover { @apply bg-red-600; }
}
.btn-blue {
  @apply bg-blue-700;

  &:hover { @apply bg-blue-600; }
}
button { @apply btn; }

.stack {
  @apply grid;

  & > * { grid-column: 1; grid-row: 1; }
}

#app header {
  text-shadow: 0 1px 1px rgba(0,0,0,0.4), 0 0 20px rgba(0,0,0,0.9);
}
</style>
