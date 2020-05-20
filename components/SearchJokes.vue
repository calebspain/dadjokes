<template>
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="text" placeholder="Search Jokes..." />
    <input type="submit" value="Serach Jokes" />
  </form>
</template>

<script>
export default {
  name: "SearchJokes",
  data() {
    return {
      text: ""
    };
  },
  methods: {
    onSubmit() {
      this.$emit("search-text", this.text);
      this.text = "";
    }
  }
};
</script>

<style>
</style>