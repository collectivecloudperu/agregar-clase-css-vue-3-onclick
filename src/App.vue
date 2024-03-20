<script>

  // Importamos 'ref'  de Vue 
  import { ref } from 'vue'

  export default {

    setup() {
      const agregar = ref(false) // Variable 'agregar' con el atributo 'ref(false)' 
      return { agregar } // Devolvemos la variable 'agregar' 
    }

  }

</script>

<template>
  <h1>Como Agregar Un Nombre De Clase Al Hacer Clic en Vue 3</h1>

  <!-- Al presiona el botón cambiamos o quitamos el nombre clase CSS -->
  <button @click="agregar = !agregar">Agregar</button> 

  <br>   

  <!-- Imagen a la cual le cambiamos el nombre de clase -->
  <img :class="{ miclase: agregar }" src="./assets/logo.jpg" width="100px">
</template>

<style>
  h1 {
    font-size: 28px;
  }

  img {
    margin-top: 30px;
  }

  /* Clase CSS */
  .miclase {
    border: solid 7px #ffa500;
  }
</style>