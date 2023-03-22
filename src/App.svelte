<script>
	export let contador = 0;

	function handleClick(){
		contador++

	}

	function reset(){
		contador = 0;
	}
</script>

<main>
	<h1>TOCA LA GALLETA CUANTAS VECES QUIERAS</h1>
	<button class="cookie-button" on:click={handleClick}></button>
	<span>{contador}</span>
	<button class="reset-button" on:click={reset}>Reiniciar</button>
    
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		
	}

	

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
	.cookie-button {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background-color: #F7D08A;
  background-image: radial-gradient(circle at 50% 50%, #F7D08A 60%, #D8A36A 100%);
  border: none;
  box-shadow: 2px 2px 5px #bfbfbf;
  position: relative;
}

.cookie-button::before {
  content: "";
  position: absolute;
  width: 60%;
  height: 60%;
  top: 20%;
  left: 20%;
  background-color: #D8A36A;
  border-radius: 50%;
  box-shadow: -2px -2px 5px #bfbfbf;
}

.cookie-button::after {
  content: "";
  position: absolute;
  width: 20%;
  height: 20%;
  top: 30%;
  left: 30%;
  background-color: #ffffff;
  border-radius: 50%;
}

.reset-button{
	display: block;
	text-align: center;
	margin: 0 auto;
	width: 80px;
	background-color: bisque;
	border: 3px solid;

}

span{
	font-size: 	400%;
	text-align: right;
	padding-left: 10%;
	font-weight: bolder;
	margin: 5px;
	color: darksalmon;

}
</style>