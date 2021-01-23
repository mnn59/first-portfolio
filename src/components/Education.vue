<template>
  <section 
  class="education-section"
  id="education">
    <v-container>
      <v-row>
        <v-col>
          <h1>Education</h1>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-timeline reverse>
            <v-timeline-item
              v-for="(year, i) in years"
              :key="i"
              :color="year.color"
              small
            >
              <template v-slot:opposite>
                <span
                  :class="`headline font-weight-bold ${year.color}--text`"
                  v-text="year.year"
                ></span>
              </template>
              <div class="py-4">
                <h2
                  :class="`headline font-weight-light mb-4 ${year.color}--text`"
                >
                  {{ year.title }}
                </h2>

                <!-- <g-image 
                src="~/helli.jpg"
                width="30"
                height="30"
                class="education-image" 
                /> -->

                <!-- <g-image :src="require(`${year.image}`)"/> -->

                <!-- <g-image 
                src="~/helli.jpg"
                width="30"
                height="30"
                class="education-image" 
                > -->

                <div>
                  {{ year.description }}
                </div>
                <v-btn tile color="success" :href="year.site" class="mt-5">
                  <v-icon left> mdi-arrow-right-box </v-icon>
                  Go to site
                </v-btn>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-col>
      </v-row>
      <br />
      <br />
    </v-container>
  </section>
</template>


<script>
export default {
  data() {
    return {
      years: [
        {
          color: "cyan",
          year: "1391-1395",
          title: "Allameh Helli High School",
          description:
            " Mathematics and Physics loremMathematics and Physics loremMathematics and Physics loremMathematics and Physics loremMathematics and Physics loremMathematics and Physics loremMathematics and Physics loremMathematics and Physics loremMathematics and Physics loremMathematics and Physics loremMathematics and Physics loremMathematics and Physics lorem",
          site: "https://helli.ir",
          image: "~/helli.jpg",
        },
        {
          color: "purple",
          year: "1396-1401",
          title: "Amirkabir University of Technology",
          description:
            "Computer Engineering lorem Computer Engineering loremComputer Engineering loremComputer Engineering loremComputer Engineering loremComputer Engineering loremComputer Engineering loremComputer Engineering lorem Computer Engineering loremComputer Engineering loremComputer Engineering loremComputer Engineering lorem",
          site: "https://aut.ac.ir/en",
        },
      ],
    };
  },
};
</script>


<style scoped>
.education-section {
  background-color: #f4fffd;
}
.education-image {
  border-radius: 3px;
  border: 1px solid black;
}
</style>
