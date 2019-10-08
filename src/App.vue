<template>
  <v-app>
    <Menu></Menu>
    <v-content id="fundo">
      <v-layout id="geral" fluid fill-height>
        <router-view />
      </v-layout>
    </v-content>
  </v-app>
</template>

<script>
import Menu from "@/components/Menu.vue";
export default {
  components: {
    Menu
  },
  data: () => ({
    //
  })
};
</script>

<style lang="scss" scoped>
* {
  font-family: "Press Start 2P", cursive;
  #fundo {
    background: url("https://i.pinimg.com/originals/dc/8d/ef/dc8def609c27f9123c4f61a83a3b93bd.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position-y: 90%;
    display: flex;
    align-items: center;

    #geral {
      background-color: white;
      border: 4px solid black;
      width: 90%;
      height: 88vh;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }
}
</style>
