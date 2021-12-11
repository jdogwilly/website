<template>
  <b-row>
    <b-col cols="2" class="text-center">
      <p class="mb-auto fs-6">{{ endDate }}</p>
      <small class="text-center">from</small>
      <p class="mt-auto fs-6">{{ startDate }}</p>
    </b-col>
    <b-col cols="10">
      <h4 class="mb-auto">{{ mainTitle }}</h4>
      <small class="mt-auto">{{ subtitle }}</small>
      <ul>
        <li v-for="bullet in bulletPoints">
          {{ bullet }}
        </li>
      </ul>
    </b-col>
  </b-row>
</template>

<script>
export default {
  props: ['startDate', 'endDate', 'mainTitle', 'subtitle', 'bulletPoints'],
}
</script>
