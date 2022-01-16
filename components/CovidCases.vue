<template>
  <div>
    <h1 class="m">Covid Cases of Japanese Prefectures</h1>
    <ul>
      <li class="covid">
        <b>{{ name_en }}:</b>
        {{getCases(cases)}}
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
      required: true,
    },
  },
  methods: {
  getCases(cases) {
  if (cases > 10000){
    return "name_en Danger!";
  } else {
    return "this.name_en Safe!";
  }
  },
  },
};
</script>


<style lang="scss">
// Store page content
.covidcases {
  display: block;
}
@import "~/node_modules/bootstrap/scss/bootstrap.scss";
@import "../assets/scss/_base.normalize.scss";
@import "../assets/scss/_components.content.scss";
@import "../assets/scss/_settings.responsive.scss";
@import "../assets/scss/_settings.variables.scss";
@import "../assets/scss/style.scss";
</style>
