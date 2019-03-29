<template>
  <div id="app">
    <app-header title="My Awards"></app-header>

    <section>
      <!-- <nav>
        <ul>
          <li>
            <a href="#">My Awards</a>
          </li>
          <li>
            <a href="#">My Next Award</a>
          </li>
          <li>
            <a href="#">Studio Website</a>
          </li>
        </ul>
      </nav>-->
      <app-nav></app-nav>

      <article>
        <h1>My Awards</h1>
        <ul class="AwardsList">
          <award-card v-for="award in awards" v-bind:key="award.id" v-bind:award="award"/>
        </ul>
      </article>
    </section>

    <app-footer></app-footer>
  </div>
</template>

<script>
import AwardCard from "./components/AwardCard.vue";
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
import AppNav from "./components/AppNav.vue";

export default {
  name: "app",
  components: {
    AwardCard,
    AppHeader,
    AppFooter,
    AppNav
  },
  data() {
    return {
      awards: [
        {
          id: 1,
          title: "High Kick",
          detail: "Kick over your head 10 times in under 10 seconds.",
          imageurl: require("./assets/high-kick.jpg")
        },
        {
          id: 2,
          title: "Closed Fist",
          detail: "Break a 1 inch wood board with closed fist.",
          imageurl: require("./assets/closed-fist.jpg")
        },
        {
          id: 3,
          title: "Dragon Spirit",
          detail: "Complete Your Form 100 Times",
          imageurl: require("./assets/dragon-spirit.jpg")
        }
      ]
    };
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  list-style-type: none;
}

body {
  font-family: Arial, Helvetica, sans-serif;
}

section {
  display: -webkit-flex;
  display: flex;
}

article {
  -webkit-flex: 3;
  -ms-flex: 3;
  flex: 3;
  background-color: #f1f1f1;
  padding: 10px;
}

@media (max-width: 600px) {
  section {
    -webkit-flex-direction: column;
    flex-direction: column;
  }
}
</style>