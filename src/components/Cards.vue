<template>
<v-card
    :loading="loading"
    class="mx-auto my-12"
    max-width="374"
  >
    <v-progress-linear
      v-if="loading"
      class="position-absolute"
      style="z-index: 1"
      color="deep-purple"
      height="10"
      indeterminate
    ></v-progress-linear>

    <v-img
      height="250"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
      cover
    ></v-img>

    <v-card-header>
      <v-card-header-text>
        <v-card-title>Cafe Badilico</v-card-title>

        <v-card-subtitle>
          <span class="mr-1">Local Favorite</span>

          <v-icon
            color="error"
            icon="mdi-fire-circle"
            size="small"
          ></v-icon>
        </v-card-subtitle>
      </v-card-header-text>
    </v-card-header>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :model-value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="text-grey ms-4">
          4.5 (413)
        </div>
      </v-row>

      <div class="my-4 text-subtitle-1">
        $ • Italian, Cafe
      </div>

      <div>Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</div>
    </v-card-text>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      loading: false,
      selection: 1,
    }),
    methods: {
      reserve () {
        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      }
    },  
  }
</script>