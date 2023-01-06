<!--Parte logica de un componente-->
<script>

  export function reciveName(name) {
    return name;
  }

  export const devTools = {
    lib1: {
      id: 1,
      name: 'svelte'
    },
    
    lib2: {
      id: 2,
      name: 'react'
    },

    lib3: {
      id: 3,
      name: 'nextJs'
    }
  }

  let count = 0;

  function clickSvelteSuma() {
    count = count + 1
  }

  function clickSvelteResta() {
    count = count - 1
    }
</script>

<!--Parte markup-->
<div>
  <h1>Hola Mundo desde Svelte! - </h1>
  <h1>Mi nombre es: { reciveName('Santi') }</h1>

  <ul>
    <li>Libreria {devTools.lib1.id}, Nombre: {devTools.lib1.name}</li>
    <li>Libreria {devTools.lib2.id}, Nombre: {devTools.lib2.name}</li>
    <li>Libreria {devTools.lib3.id}, Nombre: {devTools.lib3.name}</li>
  </ul>

  <h1>Clicks: { count }</h1>
  <button on:click={ clickSvelteSuma }> clickeame pa</button>
  <button on:click={ clickSvelteResta }> clickeame pa para restar</button>
</div>

<!--Parte estilos-->
<style>
  


</style>