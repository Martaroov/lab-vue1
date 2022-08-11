<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <MyComponent/>
    <p>{{msg}}</p>
    <input type="number" v-model="num1" :class="check"/>
    <input type="number" v-model="num2"/>
    <p>{{num1 + num2}}</p>
  </div>
</template>

<script>
// @ is an alias to /src
import MyComponent from '@/components/MyComponent.vue';

export default {
  name: 'HomeView',
  components: {
    MyComponent,
},

  data(){
    return{
      num1: 1,
      num2: 2,
      result: this.num1 + this.num2,
      msg: '2 + 2',
    }
  },
  methods:{

  },
  computed: {
    result() {
      return this.num1 + this.num2 + 3;
        },
        check() {
          if(this.num1 <5) {
            return 'danger'
          } else {
            return 'valid'
          }
        }
  }, 
};
</script>

<style>
.danger {
  border: 1px solid red;
}

.valid{
  border: 1px solid green;
}

</style>
