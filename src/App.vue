
  //v-show=""
  //v-if
  //v-else-if
  //v-else
  //diretivas 


<template>
  <TheHeader v-if="showHeader" />

  <div v-show="showName">
    Nome:{{ firstName }}<br>
    Sobrenome:{{ lastName }}

  </div>

<!--

<div v-if="acessLevel === 'admin'">Usuário Admin</div> 
<div v-else-if="acessLevel === 'marketing'">Usuário Marketing</div>
<div v-else>Usuário normal</div>

-->
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/> -->
</template>

//Single file Component - SFC
// Componentes de arquivo único

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from './components/HelloWorld.vue';
import TheHeader from './components/TheHeader.vue';

@Options({
  components: {
    HelloWorld,
    TheHeader,
  },
  data(){
    return{
      showHeader: true,
      firstName: 'John',
      lastName: 'Snow',
      showName: false,
      acessLevel: 'admin'
    }
  }


})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
