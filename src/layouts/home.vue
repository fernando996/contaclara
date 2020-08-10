<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" clipped app>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar clipped-left flat app color="transparent">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-home</v-icon>
      </v-btn>
    </v-app-bar>
    <v-parallax dark height="600" src="/pexels.png">
      <div class="white--text text-h2 font-weight-bold text-center">
        Contaclara
      </div>
      <div class="white--text subtitle-1 text-center">
        Gabinete de Contabilidade, Lda
      </div>

      <!-- <div class="white--text text-h4 font-weight-bold text-center">
        A luz que clarifica a sua contabilidade
      </div> -->
      <div class="white--text text-h5 font-weight-bold text-center">
        Serviços de contabilidade e auditoria, consultoria fiscal.
      </div>

      <!-- <v-img
        class="home-image"
        src="/pexels.jpg"
        max-height="500vh"
        gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
      ></v-img> -->
    </v-parallax>
    <v-main>
      <v-container class="pa-0 ma-0" fluid>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer absolute app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      title: 'Conta Clara',
    }
  },
}
</script>
