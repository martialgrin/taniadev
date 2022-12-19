<script>
	import { onMount } from "svelte";

	import snowGif from "./assets/images/snow.gif";
	const arrayTania = [];

	let theme = false;

	for (let i = 0; i < 15; i++) {
		arrayTania.push("TaniaPraz.ch");
	}

	// const incr = () => (counter += 1);

	// let clear;
	// $: {
	// 	clearInterval(clear);
	// 	clear = setInterval(incr, ms);
	// }
	onMount(() => {
		// flowerScene();
	});
</script>

<svelte:head>
	<title>Tania Praz</title>
	<!-- <meta name="description" content="Svelte demo app" /> -->
</svelte:head>

<div id="fixed">
	<img src={snowGif} alt="snow" />
</div>
<div id="main">
	{#each arrayTania as tania}
		<p>{tania}</p>
	{/each}
</div>

<style>
	#fixed {
		position: fixed;
		width: 100vw;
		height: 100vh;
		object-fit: cover;
	}

	img {
		width: 100vw;
		height: 100vh;
	}
	#main {
		margin: 0;
		padding: 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		height: 100vh;
	}

	p {
		text-transform: uppercase;
		white-space: nowrap;
		color: #00ff00;
		margin: 0;
		padding: 0;
	}
</style>
