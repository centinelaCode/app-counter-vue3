<script>
  
  export default {

    // FORMA 1 de crear la data (vervosa)
    // data() {
    //   return {
    //     contador: 200
    //   }
    // }

    // FORMA 2 de crear la data (resumida)
    data: () => ({
      contador: 10
    }),
    methods: {

      saludar() {
       console.log('Hola') 
      },

      incrementar() {
        this.contador ++
      },

      decrementar() {
        this.contador --
      },

      reset() {
        this.contador = 10
      },

    },
  }

</script>


<template>
  <div class="container">
    <img src="./assets//logo.svg" alt="logo vue" width="100">
    <small>
      <h1>Hola  Mundo desde Vue.js 3</h1>
    </small>
    <hr />
    <h2>Counter: <span>{{ contador }}</span> </h2>

    <!-- <button v-on:click="saludar()" >+1</button>  @ es igual que v-on:  -->
    <button @click="incrementar()">+1</button>

    <button @click="reset()">Reset</button>

    <button @click="decrementar()">-1</button>
  </div>
</template>

<style scoped>

  .container {
    text-align: center;    
  }

  small {
    color: #666;
  }

  h1 {
    font-weight: bolder;
  }

  h2 {
    font-size: 2.5rem;
  }

  span {
    color: crimson;
  }

  button {
    cursor: pointer;
    font-size: 1.5rem;
    margin: 0 6px;
  }

  
</style>