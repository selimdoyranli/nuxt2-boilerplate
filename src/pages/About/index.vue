<template lang="pug">
.page.about-page
  h1 {{ message.title }}
  p {{ message.description }}

  NuxtLink(to="/") Go to home page
</template>

<script lang="ts">
import { defineComponent, ref } from '@nuxtjs/composition-api'
import { WelcomeTypes } from './About.page.types'

export default defineComponent({
  layout: 'Default/Default.layout',
  setup() {
    const message = ref<WelcomeTypes>({
      title: 'About page',
      description: 'Welcome to about page'
    })

    return {
      message
    }
  }
})
</script>

<style lang="scss" src="./About.page.scss"></style>
