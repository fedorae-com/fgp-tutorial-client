<template>
  <v-container>
    <v-card class="mt-4 mx-auto" width="600" elevation="12">
      <v-sheet
        class="v-sheet--offset mx-auto"
        color="#1E3D58"
        elevation="12"
        max-width="calc(100% - 32px)"
      >
        <v-sparkline
          :labels="labels"
          :value="value"
          color="white"
          line-width="2"
          padding="16"
        ></v-sparkline>
      </v-sheet>

      <v-card-text class="pt-0">
        <div class="title font-weight-light mb-2">
          User Watch Time
        </div>
        <div class="subheading font-weight-light grey--text">
          Performance
        </div>
        <v-divider class="my-2"></v-divider>
        <v-icon class="mr-2" small>
          mdi-clock
        </v-icon>
        <span class="caption grey--text font-weight-light"
          >last course 26 minutes ago</span
        >
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      labels: ["12am", "3am", "6am", "9am", "12pm", "3pm", "6pm", "9pm"],
      value: [200, 675, 410, 390, 310, 460, 250, 240]
    };
  }
};
</script>

<style lang="css" scoped>
.v-sheet--offset {
  top: -24px;
  position: relative;
}
</style>
