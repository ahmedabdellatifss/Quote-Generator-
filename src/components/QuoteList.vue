<template>
  <section class="quote-list">
    <div class="quote" v-for="(quote, i) in quotes.slice().reverse()" :key="i">
      <div class="quote-header">
        {{ quote.content }}
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: ["quotes"],
};
</script>

<style scoped>
.quote-list {
  padding: 32px;
  max-width: 720px;
  margin: 0 auto;
}
.quote-list .quote {
  background-color: #EEE;
  padding: 16px;
  border-radius: 16px;
  margin-bottom: 16px;
}
.quote-list .quote-header {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  line-height: 1.2em;
  max-height: 1.2em;
}
.quote-list .quote:hover .quote-header {
  white-space: unset;
  max-height: unset;
}
</style>
