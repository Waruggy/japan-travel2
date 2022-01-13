<template>
  <div class="container">
     <div class="row">
          <!-- Image with text -->
          <div class="col">
            <ImageTemplate :source="'mtfuji.jpg'" :message="'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.'" :title="'Mt. Fuji'" :desc="'Image of Mt. Fuji'"/>
            <ImageTemplate :source="'tokyo.jpg'" :message="'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.'" :title="'Tokyo'" :desc="'Image of Tokyo'"/>
          </div>
      </div>
      <!-- Footer -->
    <div class="row bg-light text-middle">
      &copy;2021 Japan Travel, LLC | Seattle, WA
    </div>
  </div>
</template>

<script>
import ImageTemplate from '../components/Image.vue'
export default {
  name: 'BlogPage',
  components: {ImageTemplate},
  paragraph: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import "../assets/scss/_base.normalize.scss";
@import "../assets/scss/_components.content.scss";
@import "../assets/scss/_settings.responsive.scss";
@import "../assets/scss/_settings.variables.scss";
@import "../assets/scss/style.scss";
</style>
