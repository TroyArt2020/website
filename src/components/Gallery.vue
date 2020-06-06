<template lang="pug">
#gallery
  #loader(class="flex justify-center items-center")
    .spinner(class="w-32 h-32 border-8")
  #images(class="flex flex-wrap justify-between hidden")
    template(v-for="image in images")
      a.overlay(class="w-full md:w-auto mb-3 stack" :href="`${image.url}.jpg`" target="_blank")
        img(class="w-full md:w-auto" :src="`${image.url}b.jpg`")
        .attributions(class="bg-white bg-opacity-75 flex flex-col items-center justify-center w-full h-full" :class="image.attributions.length > 0 ? 'has-attributions' : ''")
          template(v-for="attribution in image.attributions")
            span(class="text-center") {{ attribution }}
</template>

<script>
export default {
  props: ['images'],
  mounted: function() {
    const galleryElement = document.getElementById('gallery');
    const imageElements  = galleryElement.getElementsByTagName('img');
    const loaderElement  = document.getElementById('loader');
    const imagesElement  = document.getElementById('images');
    let   imagesLoaded   = 0;

    for (let imageElement of imageElements) {
      imageElement.onload = () => {
        imagesLoaded++;

        if (imagesLoaded == this.images.length) {
          loaderElement.classList.add('hidden');
          imagesElement.classList.remove('hidden');
        }
      }
    }
  },
}
</script>

<style scoped>
.overlay {
  & .attributions { opacity: 0; }

  &:hover {
    & .has-attributions { opacity: 1; }
  }
}

.spinner { /* Use width/height/border-width utilities to customize */
  border-radius: 50%;
  border-color: #cbd5e0; /* border-gray-400 */
  border-top-color: #4a5568; /* border-gray-700 */
  animation: 2s rotate-cw infinite linear;
}

@keyframes rotate-cw {
  0%   { transform: rotate(0); }
  100% { transform: rotate(360deg); }
}
</style>

