<script>

	let contador = 0;
	let textColor ='text-primary';
	const aumentar = ()=>{
		contador++;
	}
	$:dobrou = contador*2;
	$:if(contador > 5){
		textColor='text-mudanca';
	}
</script>

<main>
	<h1>TESTANDO</h1>
	<h2>RESULTADO: {contador}</h2>
	<h2 class={textColor}>RESULTADO EM DOBRO: {dobrou}</h2>
	<button on:click={aumentar}>CLIQUE AQUI</button>
</main>

<style>
	.text-primary {
		color: black;
	}
	.text-mudanca{
		color: red
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>