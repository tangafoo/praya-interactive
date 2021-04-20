<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-toolbar-title>Praya Lane Interactive - 20209307</v-toolbar-title>
      </div>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <v-container class="grey lighten-5">
        <v-row no-gutters>
          <v-col v-for="tour in tours" :key="tour.tourName" cols="12" sm="4">
            <TourCard v-bind="tour" />
          </v-col>
        </v-row>
      </v-container>
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import TourCard from "./components/TourCard";
import Footer from "./components/Footer";

export default {
  name: "App",

  components: {
    TourCard,
    Footer,
  },

  data: () => ({
    tours: [
      {
        tourName: "Sun Bear, Borneo",
        tourDescription:
          "You will be guided through a journey at the center where you will get to take a closer look at the at sun bear's movement, their natural habitat, and also, how they interact with each other. Besides that, I will be share some information about our local flora and fauna such as orangutans, macaques, squirrels and diverse tropical tree species. If we are lucky enough, we may get to see some snakes taking its meal of the day.",
        tourImageUrl:
          "https://production-buddyz.s3.ap-southeast-1.amazonaws.com/store/cf6bd56477ffe6cad4ebb7e965065076.jpg",
        tourPrice: "RM120",
        tourRating: 3.5,
        ratingNumbers: 213,
      },
      {
        tourName: "Rubber Tapping & Outskirts Cycling Adventure, Melaka",
        tourDescription:
          "Our first stop will be at a rubber estate, where I will show how rubber trees are tapped, then you will get to try it yourself with the equipment used to tap rubber trees. After that, we will cycle along the banks of the river and pass through the small villages with plenty of opportunities to stop for photos. The last stop of the journey will be a scenic break at the paddy field and we will turn back toward the meeting point on a different road as we cycle through back roads and narrow streets to further immerse yourself in a rural way of life.",
        tourImageUrl:
          "https://production-buddyz.s3.ap-southeast-1.amazonaws.com/store/e86339ffdd0812d280bf43b1ce939624.jpeg",
        tourPrice: "RM150",
        tourRating: 3,
        ratingNumbers: 50,
      },
      {
        tourName: "Praya Lane, Melaka",
        tourDescription:
          "Come join me on this virtual experience, yes, it is LIVE ON-SITE (not a webinar or pre-recorded) and we will get to engage into interesting conversation about the history and lifestyle at Praya Lane. To sweeten the experience, we will have a virtual yum-cha (tea-time) with a lovely family who is still living in a 100-year-old residential property.",
        tourImageUrl:
          "https://production-buddyz.s3.ap-southeast-1.amazonaws.com/store/cc3d425b636e08544a4d87dbf4fddb0d.jpg",
        tourPrice: "RM50",
        tourRating: 5,
        ratingNumbers: 1805,
      },
    ],
  }),
};
</script>
