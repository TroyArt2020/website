<template lang="pug">
#gallery(class="flex flex-wrap justify-between")
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
}
</script>

<style scoped>
.overlay {
  & .attributions { opacity: 0; }

  &:hover {
    & .has-attributions { opacity: 1; }
  }
}
</style>

