<template>
  <v-card :loading="loading" class="mx-auto my-12" max-width="374">
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img height="250" :src="tourImageUrl"></v-img>

    <v-card-title>{{ tourName }}</v-card-title>
    <v-card-subtitle>{{ tourPrice }}</v-card-subtitle>

    <v-card-text>
      <v-row align="center" class="mx-0">
        <v-rating
          :value="tourRating"
          color="amber"
          background-color="grey-lighten"
          dense
          half-increments
          readonly
          size="18"
        ></v-rating>

        <div class="grey--text ml-4">
          {{ tourRating }} ({{ ratingNumbers }})
        </div>
      </v-row>

      <div class="my-4 subtitle-1"></div>

      <div>
        {{ tourDescription }}
      </div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title>Virtual tour times</v-card-title>

    <v-card-text>
      <v-chip-group
        v-model="selection"
        active-class="deep-purple accent-4 white--text"
        column
      >
        <v-chip>5:30PM</v-chip>

        <v-chip>7:30PM</v-chip>

        <v-chip>8:00PM</v-chip>

        <v-chip>9:00PM</v-chip>
      </v-chip-group>
    </v-card-text>

    <v-card-actions>
      <v-btn color="deep-purple lighten-2" text @click="startTour">
        Start Tour
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    tourName: String,
    tourDescription: String,
    tourImageUrl: String,
    tourPrice: String,
    tourRating: Number,
    ratingNumbers: Number,
  },
  methods: {
    startTour() {
      window.open(
        "https://prayalane.h5p.com/content/1291293100404506089",
        "_blank"
      );
    },
  },
};
</script>