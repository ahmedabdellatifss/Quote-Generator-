<template>
  <section class="quote">
    <div class="quote-content">
      {{ quote.content }}
    </div>
    <div class="quote-info">
      <div class="quote-info-anime">
        {{ quote.anime }}
      </div>
      <div class="quote-info-author">
        {{ quote.character }}
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: ["quote"],
};
</script>

<style scoped>
.quote {
  position: relative;
  padding: 32px;
  margin: 0 auto;
  max-width: 720px;
}
.quote-content {
  position: relative;
  font-size: 1.5em;
  font-weight: 700;
  background-color: #131A26;
  color: #EEE;
  padding: 48px 32px;
  border-radius: 16px;
}
.quote-content:before,
.quote-content:after {
  content: '"';
  color:#848484;
  margin: 0 2px;
}
.quote-info {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  padding: 32px;
}
.quote-info-author,
.quote-info-anime {
  position: absolute;
  padding: 12px 16px;
  font-size: 1.2em;
  font-weight: 400;
  border-radius: 99px;
  color:#EEE;
  text-align: center;
}
.quote-info-author {
  top: calc(100% - 32px);
  right: 0px;
  transform: translateY(-50%);
  background-color: #8A4FFF;
}
.quote-info-anime {
  top: 0px;
  left: 0px;
  background-color: #32CBFF;
  color: #131A26;
}
</style>
