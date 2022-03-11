<template>
  <div class="container">
    <input type="number" placeholder="Valor 1" v-model="value1" />
    <input type="number" placeholder="Valor 2" v-model="value2" />
    <div class="result">Resultado: {{ result }}</div>
  </div>
</template>

<script lang="ts">
import { Vue } from "vue-property-decorator";

const HelloWorld = Vue.extend({
  data: () => ({
    value1: 5,
    value2: 8,
  }),
  computed: {
    result() {
      return Number(this.value1) + Number(this.value2);
    },
  },
});

export default HelloWorld;
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
