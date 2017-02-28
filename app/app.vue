<template lang="html">
  <div class="app">
    <div class="grid">
      <div class="grid__item grid__item--sidebar">
        <div class="Profile">
          <img src="http://fillmurray.com/400/400" alt="" class="Profile__pic">

          <h2 class="Profile__username">{{profile.username}}</h2>
        </div>
      </div>
      <div class="grid__item grid__item--main">
        <!-- <p :class="profile.username">HELLO</p> -->
        <repo-card v-bind:repo="{name: 'Spoon-Knife'}"></repo-card>
        <repo-card v-bind:repo="{name: 'Hello-World'}"></repo-card>
      </div>
    </div>
  </div>
</template>

<script>
import RepoCard from './repo-card.vue';

export default {
  components: {
    RepoCard,
  },

  data() {
    return {
      profile: {
        username: 'MurrayFan85'
      },
    };
  },

  methods: {

  },
};
</script>
