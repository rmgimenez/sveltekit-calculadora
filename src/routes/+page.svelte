<script>
	import Calculadora from '$lib/components/Calculadora.svelte';
</script>

<svelte:head>
	<title>Svelte - Calculadora</title>
	<meta name="description" content="Projeto Svelte - Caculadora" />
</svelte:head>

<main>
	<Calculadora />
</main>

<style>
	:global(body) {
		background-color: black;
		font-family: 'Roboto', sans-serif;
	}
	:root {
		--cor-fundo: #555;
	}
	main {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}
</style>
