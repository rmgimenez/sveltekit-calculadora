<script>
	import Botao from './Botao.svelte';
	import Linha from './Linha.svelte';
	import Tela from './Tela.svelte';

	let valor = 0;

	function numeroDigitado(numero) {
		valor += numero;
	}
</script>

<div class="calculadora">
	<Tela {valor} />
	<Linha>
		<Botao texto="AC" triplo destaque />
		<Botao texto="/" operacao />
	</Linha>
	<Linha>
		<Botao onClick={numeroDigitado} texto="7" />
		<Botao onClick={numeroDigitado} texto="8" />
		<Botao onClick={numeroDigitado} texto="9" />
		<Botao onClick={numeroDigitado} texto="*" operacao />
	</Linha>
	<Linha>
		<Botao texto="4" />
		<Botao texto="5" />
		<Botao texto="6" />
		<Botao texto="+" operacao />
	</Linha>
	<Linha>
		<Botao texto="1" />
		<Botao texto="2" />
		<Botao texto="3" />
		<Botao texto="-" operacao />
	</Linha>
	<Linha>
		<Botao texto="0" duplo />
		<Botao texto="," />
		<Botao texto="=" destaque />
	</Linha>
</div>

<style>
	.calculadora {
		background-color: var(--cor-fundo);
		height: 140px;
		width: 150px;
		display: flex;
		flex-direction: column;
		padding: 10px;
		border-radius: 10px;
	}
</style>
