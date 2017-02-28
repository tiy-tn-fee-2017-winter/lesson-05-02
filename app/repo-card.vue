<template lang="html">
  <div class="RepoCard">
    <h2 class="RepoCard__name">{{repo.name}}</h2>
    <h4 class="RepoCard__description">{{repo.description}}</h4>

    <p class="Level">
      <span class="Level__item">
        <span class="Dot"></span>
        {{repo.language}}
      </span>
      <span class="Level__item">
        <span class="fa fa-star"></span>
        {{repo.stars}}
      </span>
      <span class="Level__item">
        <span class="fa fa-fork"></span>
        {{repo.forks}}
      </span>
    </p>
  </div>
</template>

<script>
export default {
  // Define arguments that are accepted for this component
  props: ['repo'],

  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
