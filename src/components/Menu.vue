<template>
  <div>
    <v-navigation-drawer v-model="drawer" id="menu" absolute left temporary>
      <v-list nav dense>
        <v-list-item-group
          v-for="item in items"
          :key="item.title"
          :to="item.rota"
          class="menu-item"
        >
          <v-list-item>
            <!-- <v-icon>{{ item.icon }}</v-icon> -->
            <p>{{ item.title }}</p>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <!-- Menu -->
    <v-toolbar id="menu-topo" color="#6666ff" dark fixed>
      <v-toolbar-title class="ml-0">
        <v-app-bar-nav-icon
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon> </v-toolbar-title
      >Menu
    </v-toolbar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        { title: "Perfil", icon: "nes-smartphone", rota: "/" },
        {
          title: "Formação / Certificados",
          icon: "nes-mario",
          rota: "/certificados"
        },
        {
          title: "Experiência",
          icon: "nes-icon close is-large",
          rota: "/experiencia"
        },
        { title: "Competências", icon: "nes-mario", rota: "/competencias" },
        { title: "Projetos", icon: "nes-mario", rota: "/projetos" }
      ]
    };
  }
};
</script>

style
<style lang="scss" scoped>
#menu {
  font-family: "Press Start 2P", cursive;
  font-size: 14px;
  #menu_item {
    display: inline-flex;
    .icone {
      width: 10px;
    }
  }
}
#menu-topo {
  box-shadow: 7px 5px #333333;
  border-right: 5px solid #333333;
}
</style>
