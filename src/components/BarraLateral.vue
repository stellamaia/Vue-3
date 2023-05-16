<template>
  <header>
    <h1>
      <div class="content-img">
        <img src="@/assets/logo.png" alt="logo">
      </div>
    </h1>
    <v-switch
    v-model="model"
    inset
    :label="textoBotao"
    class="button" @click="alterarTema"
  ></v-switch>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  name: 'BarraLateral',
  emits: ['aoTemaAlterado'],
  data() {
    return {
      modoEscuroAtivo: false,
      model: false
    }
  },
  computed: {
    textoBotao() {
      if (this.modoEscuroAtivo) {
        return 'Desativar modo escuro'
      }else {
        return 'Ativar modo escuro'
      }
    }
  },
  methods: {
    alterarTema() {
      this.modoEscuroAtivo = !this.modoEscuroAtivo
      this.$emit('aoTemaAlterado', this.modoEscuroAtivo);
    }
  }
});


</script>
<style scoped>

header{
  background:#0d3b66;
  width: 100%;
  height: 100vh;
  text-align: center;
  
}
img{
  height:50px;
}
.content-img{
  display: flex;
    justify-content: center;

} 
@media only screen and (max-width:768px){
  header{
    padding: 2.5rem;
    height: auto;
  }
}
@media only screen and (min-width:1024px){
  header{
    padding: 2.5rem;
   
  }
}
.button{
  margin-top: 20px;
  background-color: rgba(52, 76, 97, 0);
  border: none;
  color: white;
}


</style>