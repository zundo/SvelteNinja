<script>
	export let name;
	const clickTitle = () =>{
		console.log("OK");
	}
</script>

<main>
{#if name === 'Mike'}
	<h1 class="isMike" on:click={clickTitle}>Hello {name}!</h1>
{:else}
	<h1 on:click={clickTitle}>Hello {name}!</h1>	
{/if}

	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<input type="text" bind:value={name} >
</main>

<style>
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
	.isMike{
		color: #ff2fff
	}
</style>