<template>
  <div>
      Clicked:{{count}} times,count is {{evenOrOdd}}
      <div>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    </div>
  </div>
</template>

<script>
import {mapState,mapActions, mapGetters} from 'vuex';

export default {
    computed:{
        ...mapState(['count']),
        ...mapGetters(['evenOrOdd'])
    },
    methods:{
        ...mapActions(['increment','decrement'])
    }
}
</script>

<style>

</style>