<template>
  <v-container>
    <div class="text-h3 pb-4">
      Os nossos serviços
    </div>
    <v-row>
      <v-col v-for="n in 4" :key="n">
        <v-card shaped color="cyan lighten-4">
          <v-card-title>Serviço {{ n }}</v-card-title>
          <v-card-text
            >Lorem ipsum dolor sit, amet consectetur adipisicing elit. Et nobis
            officiis veniam, dolorem, quia nostrum facere consequuntur
            provident, ipsa modi velit quaerat sint atque minima recusandae
            quisquam. Ullam, voluptatem unde.</v-card-text
          >
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  layout: 'home',
}
</script>
