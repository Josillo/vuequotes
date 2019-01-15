<template>
  <div class="row">
    <app-quote
      v-for="(quote, index) in quotes"
      @click.native="deleteQuote(index);"
    >
      {{ quote }}</app-quote
    >
  </div>
</template>
<script>
import Quote from "./Quote.vue";
export default {
  props: ["quotes"],
  components: {
    appQuote: Quote
  },
  methods: {
    deleteQuote(index) {
      this.$emit("quoteDeleted", index);
    }
  }
};
</script>
<style>
.panel-body {
  color: #6e6e6e;
  font-size: 24px;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: #ffe2e2;
}
</style>
