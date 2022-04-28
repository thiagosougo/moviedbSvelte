<script lang="ts">
  import Botao from "./components/Botao.svelte";
  import Calculadora from "./components/Calculadora.svelte";
</script>

<main>
  <Calculadora />
</main>

<style>
	:root{
		--cor-fundo: #555
	}
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;

    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }

  :global(body){
	  background-color: black
  }
</style>

