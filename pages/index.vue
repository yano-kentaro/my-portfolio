<template>
  <v-container>
    <div style="width: 100%; display: flex">
    <v-card
      width="60%"
    >
      <v-img
        src="Typie.png"
      />
    </v-card>

    <v-card
      width="30%"
    >
      <v-img
        src="qiita-icon2.png"
      />
    </v-card>
    </div>
  </v-container>
</template>

<script>
export default {
  data: function() {
    return {
    }
  }
}
</script>

<style scoped>
.container{
  height: 80vh;
  background-color: rgba(223, 223, 223, 0.3);
  overflow: scroll;
  margin-top: 5vh;
}

.row-eq-height {
  display: flex;
  flex-wrap: wrap;
}

.v-card {
  margin: 1%;
}
</style>
