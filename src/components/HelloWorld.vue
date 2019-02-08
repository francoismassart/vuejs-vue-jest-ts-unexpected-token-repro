<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <b-table striped hover :items="items"></b-table>
  </div>
</template>

<script lang="ts">
import bTable from 'bootstrap-vue/es/components/table/table';
import Vue from 'vue';

const demoItems = [
  { isActive: true, age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
  { isActive: false, age: 21, first_name: 'Larsen', last_name: 'Shaw' },
  { isActive: false, age: 89, first_name: 'Geneva', last_name: 'Wilson' },
  { isActive: true, age: 38, first_name: 'Jami', last_name: 'Carney' },
];

export default Vue.extend({
  name: 'HelloWorld',
  components: {
    bTable,
  },
  props: {
    msg: String,
  },
  data() {
    return {
      items: demoItems,
    };
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
