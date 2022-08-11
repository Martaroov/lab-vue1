<template>
  <div>
      <h3>Este es mi componente</h3>
      <p>El número es {{numero}}  </p>
      <button @click="sumar">Sumar</button>
      <button @click="restar"> Restar</button>
  </div>
</template>

<script>
export default {
    data(){
        return{
           numero: 34,
        };
    },
    methods: {
        sumar() {
            this.numero ++;
        },
        restar () {
            this.numero --;
        },
    },
};
</script>

<style>

</style>