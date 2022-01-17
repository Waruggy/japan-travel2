<template>
  <div>
    <h1 class="m">Covid Cases of Japanese Prefectures</h1>
    <ul>
      <li class="covid">
      <div v-for="element in prefecture" v-bind:key="element.id">
        <b>{{ element.name_en }}:</b>
        {{getCases(element.cases)}}
      </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
    };
  },
  name: "CovidCases",
  // Set component props
  props: {
    prefecture: {
      type: Array,
      required: true,
    },
  },
  methods: {
  getCases(cases) {
  if (cases > 10000){
    return "Danger!";
  } else {
    return "Safe!";
  }
  },
  },
};
</script>


<style lang="scss" scoped>
// Store page content
.covid {
  display: block;
}
@import "~/node_modules/bootstrap/scss/bootstrap.scss";
@import "../assets/scss/_base.normalize.scss";
@import "../assets/scss/_components.content.scss";
@import "../assets/scss/_settings.responsive.scss";
@import "../assets/scss/_settings.variables.scss";
@import "../assets/scss/style.scss";
</style>
