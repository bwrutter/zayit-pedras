<template>
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
<style scoped>
.whatsapp-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 1000;
}
</style>

