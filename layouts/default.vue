<template>
  <v-app>
    <v-main id="bg-img">
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>

<style scoped>
#bg-img {
  background-image: url(/congruent_pentagon.png);
  background-repeat: repeat;
}
</style>
