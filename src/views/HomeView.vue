<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">

    <Contador/>

   

    <div class="cuadrado">
      {{$store.state.counter}} <sup>2</sup> = {{$store.getters.cuadrado}};
    </div>

    <div class="botones">
      <button @click="$store.dispatch('bajarContador')">-</button>
      <button @click="$store.dispatch('subirContador')">+</button>
      <button @click="$store.commit('resetear')">Reset</button>
    </div>
    
  </div>
</template>

<script>
import Contador from "../components/Contador.vue";
export default {
  name: 'HomeView',
  components:{
    Contador,
  }
}

</script>


<style>
div{
  margin-bottom: 10px;
}

.counter{
    font-size: 80px;
}

.botones button{
  font-size: 40px;
  width: 120px;
  margin: 0px 10px;
}

.cuadrado{
  font-size:25px;
}

</style>