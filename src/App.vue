<template>
  <div>
    <!--
      -
      <app-header
        v-bind:title="title"
        v-on:changeTitle="updateTitle($event);"
      ></app-header>
      <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>
      <app-footer v-bind:title="title"></app-footer>
    -->
    <app-helper>
      <h2 slot="title">This title is from app</h2>
      <p slot="paragraph">Experimental purpose testing needs....</p>
    </app-helper>
  </div>
</template>

<script>
// Imports
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Ninjas from "./components/Ninjas.vue";
import HelperComponent from "./components/helperComponent.vue";
export default {
  components: {
    "app-header": Header,
    "app-footer": Footer,
    "app-ninjas": Ninjas,
    "app-helper": HelperComponent
  },
  data() {
    return {
      title: "vuejs",
      ninjas: [
        { name: "Ryu", speciality: "Vue Components", show: false },
        { name: "Crystal", speciality: "HTML Wizardry", show: false },
        { name: "Hitoshi", speciality: "Click Events", show: false },
        { name: "Tango", speciality: "Conditionals", show: false },
        { name: "Kami", speciality: "Webpack", show: false },
        { name: "Yoshi", speciality: "Data Diggin", show: false }
      ]
    };
  },
  methods: {
    updateTitle: function(updatesTitle) {
      this.title = updatesTitle;
    }
  }
};
</script>

<style>
body {
  margin: 0;
  font-family: "Nunito SemiBold";
}
</style>
