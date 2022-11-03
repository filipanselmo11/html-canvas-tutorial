<template>
  <div class="hello">
    <h1>HELLO WORLD</h1>
    <button type="button" @click="printScreen">
      Tirar Print
    </button>
  </div>
</template>

<script>
import html2canvas from 'html2canvas';
export default {
  name: 'HelloWorld',
  methods: {
    async printScreen() {
      await html2canvas(document.body).then((canvas) => {
        document.body.appendChild(canvas);
      });
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
