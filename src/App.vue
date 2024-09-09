<script>
/* 
  Per importare ed utilizzare un componente dentro un altro devo:
  1) Importazione del componente
  2) Dichiarazione del componente
  3) Utilizzo del componente
*/

// 1) Importazione del componente
import AppTitle from './components/AppTitle.vue';

export default {
  data() {
    return{
      count: 0
    }
  },

  // 2) Dichiarazione del componente
  components: {
    AppTitle
  },
  methods: {
    incrementCount() {
      this.count++;
    }
  }
}
</script>

<template>
  <!-- 3) Utilizzo del componente -->
  <AppTitle />

  <div>

    <button @click="incrementCount()">
      {{ count }}
    </button>

  </div>

</template>

<style scoped>
div {
  text-align: center;
}
</style>
