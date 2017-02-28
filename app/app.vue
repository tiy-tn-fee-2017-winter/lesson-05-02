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
        <repo-card v-for="current in repositories" v-bind:repo="current"></repo-card>
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

  // This method will run every time a new instance of this component is CREATED
  // This is run AFTER `data`
  created() {
    fetch('http://api.github.com/users/octocat/repos')
      .then(response => response.json())
      .then((repos) => {
        this.repositories = repos;
      });
  },

  data() {
    return {
      profile: {
        username: 'MurrayFan85'
      },

      repositories: [
        { name: 'Spoon-Thing' },
        { name: 'A New Thing' },
        { name: 'Hello-World' }
      ],
    };
  },

  methods: {

  },
};
</script>
