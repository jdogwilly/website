<template>
  <Resume v-bind:blurbs="resumeBlurb" showEmail showPhone />
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data: function () {
    return {
      resumeBlurb: [
        `Experienced software engineer with 2 years of
experience running a large distributed system, supporting the largest catalog
on earth. I started working for my parent's company (Doctor Electric)
developing their website and grew to influence their growing IT needs. I've
designed a number of applications to fill data analytics and reporting
requirements. At Amazon, I've worked on code updates to 15+ year old systems
and cutting edge distributed computing services. In my freetime, I am likely
tinkering with my smart home, playing with my cats, or playing a good game.
While I enjoy my job now, I've always been more interested in lighter and more
flexible environments as well as embeded systems.`,
      ],
    }
  },
})
</script>
