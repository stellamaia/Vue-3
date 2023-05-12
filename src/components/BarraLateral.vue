<template>
  <header>
    <h1>
      <div class="content-img">
        <img src="@/assets/logo.png" alt="logo">
      </div>
    </h1>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  name: 'BarraLateral',
});

</script>
<style scoped>

header{
  background:#0d3b66;
  width: 100%;
  height: 100vh;
  
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



</style>