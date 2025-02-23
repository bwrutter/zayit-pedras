<template>
  <v-row class="mt-2 ml-1 mr-1">
    <v-col v-for="(card, index) in cards" :key="index">
      <v-card class="mx-auto" max-width="170">
        <v-img :src="getImage(card.img)" height="250px" cover />

        <v-card-title>
          {{ card.title }}
        </v-card-title>

        <v-card-subtitle>
          {{ card.subtitle }}
        </v-card-subtitle>

        <v-card-actions>
          <v-btn color="orange-lighten-2" text="Detalhes" @click="toggleShow(index)" />

          <v-spacer />

          <v-btn :icon="show[index] ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="toggleShow(index)" />
        </v-card-actions>

        <v-expand-transition>
          <div v-show="show[index]">
            <v-divider />
            <v-card-text>{{ card.description }}</v-card-text>
          </div>
        </v-expand-transition>
      </v-card>
    </v-col>
  </v-row>
  <v-btn
    href="https://api.whatsapp.com/send?phone=47920028440&text=Olá,%20gostaria%20de%20saber%20mais%20sobre%20seus%20serviços!"
    target="_blank"
    fab
    color="green"
    class="whatsapp-button"
  >
    <v-icon>mdi-whatsapp</v-icon>
  </v-btn>
</template>

<script>
export default {
  data() {
    return {
      show: [],
      cards: [
        {
          img: 'img-1.jpeg',
          title: 'Arvore',
          subtitle: 'Esmeralda com quartzos',
          description:
            "Uma bela arvore que significa xxx",
        },
        {
          img: 'img-2.jpg',
          title: 'Quartzo',
          subtitle: 'Quartzo em uma base',
          description:
            "Uma quartzo blablabla",
        },
        {
          img: 'img-3.jpg',
          title: 'Arvore',
          subtitle: 'Esmeralda com quartzos',
          description:
            "Uma bela arvore que significa xxx",
        },
        {
          img: 'img-4.jpg',
          title: 'Arvore',
          subtitle: 'Esmeralda com quartzos',
          description:
            "Uma bela arvore que significa xxx",
        },
        {
          img: 'img-5.jpg',
          title: 'Quartzo',
          subtitle: 'Quartzo em uma base',
          description:
            "Uma quartzo blablabla",
        },
        {
          img: 'img-6.jpg',
          title: 'Arvore',
          subtitle: 'Esmeralda com quartzos',
          description:
            "Uma bela arvore que significa xxx",
        },
        {
          img: 'img-6.jpg',
          title: 'Arvore',
          subtitle: 'Esmeralda com quartzos',
          description:
            "Uma bela arvore que significa xxx",
        },
        {
          img: 'img-6.jpg',
          title: 'Arvore',
          subtitle: 'Esmeralda com quartzos',
          description:
            "Uma bela arvore que significa xxx",
        },
        {
          img: 'img-6.jpg',
          title: 'Arvore',
          subtitle: 'Esmeralda com quartzos',
          description:
            "Uma bela arvore que significa xxx",
        },
        {
          img: 'img-6.jpg',
          title: 'Arvore',
          subtitle: 'Esmeralda com quartzos',
          description:
            "Uma bela arvore que significa xxx",
        },
      ],

    };
  },
  methods: {
    toggleShow(index) {
      this.show[index] = !this.show[index];
    },
    getImage(image) {
      //return `/public/${image}`;
      return `${image}`;
    },
  },
}
</script>
<style scoped>
.whatsapp-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 1000;
}
</style>
