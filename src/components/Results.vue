<template>
  <p>Reaction time - {{score}} ms</p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null,

    }
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "Wow, that's fast! 🙀"
    } else if (this.score < 400) {
      this.rank = "Pretty good...Could be faster though 😼"
    } else {
      this.rank = "So slow... 😹"
    }
  }
}
</script>

<style>
  .rank {
    font-size: 1.4rem;
    color: rgb(113, 151, 233);
    font-weight: bold;
  }
</style>