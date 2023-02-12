<template lang="pug">
.page.home-page
  h1 {{ message.title }}
  p {{ message.description }}

  NuxtLink(to="/about") Go to about page
</template>

<script lang="ts">
import { defineComponent, ref } from '@nuxtjs/composition-api'
import { WelcomeTypes } from './Home.page.types'

export default defineComponent({
  layout: 'Default/Default.layout',
  setup() {
    const message = ref<WelcomeTypes>({
      title: 'Home page',
      description: 'Welcome to home page'
    })

    return {
      message
    }
  }
})
</script>

<style lang="scss" src="./Home.page.scss"></style>
