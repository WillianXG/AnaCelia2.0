<template>
  <v-app>
    <v-app-bar app color="#000000" dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Ana Celia Psicologa</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app>
      <v-list>
        <v-list-item link to="/">
          <v-list-item-icon>
          </v-list-item-icon >
          <v-list-item-title>Início</v-list-item-title>
        </v-list-item>
        <v-list-item link to="/about">
          <v-list-item-icon>
          </v-list-item-icon>
          <v-list-item-title>Sobre</v-list-item-title>
        </v-list-item>
        <v-list-item link to="/treatment">
            <v-icon>mdi-settings</v-icon>
          <v-list-item-title>Tratamentos</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-content>
      <!-- Conteúdo principal do seu aplicativo aqui -->
      <div class="text-center mt-15">
        <NuxtPage/>
      </div>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
    };
  },
};
</script>


<style>
/* Estilo para ocultar a barra de rolagem vertical */
.v-application {
  overflow-y: hidden;
}
</style>