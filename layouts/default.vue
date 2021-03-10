<template>
  <v-app>
    <v-main id="bg-img">
      <v-app-bar color="success" app>
        <v-app-bar-nav-icon @click="toggleNaviFlag" />
        <v-app-bar-title class="font">My Portfolio</v-app-bar-title>
      </v-app-bar>

      <v-navigation-drawer
        v-model="navigationFlag"
        color="green accent-2"
        app
        disable-resize-watcher
        >
        <v-list rounded style="padding: 10%;">
          <v-subheader
            class="font"
            style="font-size: 1.5rem; color: white;"
            v-text="subHeaderText" />
          <v-divider />
          <v-list-item-group>
            <v-list-item
              v-for="(item, i) in items"
              :key="i"
              class="font"
              style="margin: 10% 0; transition: all .3s ease">
              <v-list-item-title
                v-text="item.text"
                style="font-size: 1.2rem;" />
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>

      <nuxt />

    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      navigationFlag: false,
      items: [{ text: "自己紹介" },
              { text: "これまでの経歴" },
              { text: "Qiita投稿記事" },
              ],
      subHeaderText: "CONTENTS",
    }
  },
  methods: {
    toggleNaviFlag: function() {
      this.navigationFlag = !this.navigationFlag
    }
  },
}
</script>

<style scoped>
#bg-img {
  background-image: url(/congruent_pentagon.png);
  background-repeat: repeat;
}

.font {
  font-weight: bold;
  letter-spacing: 1px;
}

.v-list-item:hover {
  background-color: #00E676;
}

</style>
