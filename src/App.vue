<template>
  <v-app>
    <v-app-bar app>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-spacer></v-spacer>

      <v-btn href="#" target="_blank" text>
        <span class="mr-2">Inicio</span>
      </v-btn>
      <v-btn href="#" target="_blank" text>
        <span class="mr-2">Buscar</span>
      </v-btn>
      <v-btn href="#" target="_blank" text>
        <span class="mr-2">Acerca de</span>
      </v-btn>
    </v-app-bar>

    <v-main class="mt-10">
      <v-container>
        <v-row>
          <v-col cols="4" v-for="(item, index) of productos" :key="index">
            <v-card>
              <v-img :src="item.img" height="370px"></v-img>
              <v-card-title>{{ item.name }}</v-card-title>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    productos: [
      {
        name: "Salchicha",
        img:
          "https://previews.123rf.com/images/capturelight/capturelight1212/capturelight121200008/16733056-norma-de-pelo-corto-perro-salchicha-en-el-jard%C3%ADn.jpg",
      },
      {
        name: "Salchicha pelo duro",
        img:
          "https://nfnatcane.es/blog/wp-content/uploads/2019/09/perro-teckel-de-cuerpo-completo.jpg",
      },
      {
        name: "Salchicha pelo largo",
        img:
          "https://www.mundoperros.es/wp-content/uploads/2016/04/perro_pelo_largo.jpg.webp",
      },
      {
        name: "Cachorro salchicha",
        img:
          "https://www.perros2.com/wp-content/uploads/2011/12/teckel-dachshund-salchicha.jpg",
      },
    ],
  }),
};
</script>
