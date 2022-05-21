<script>
	import Example2 from "./Example2.svelte";
	export let name;

	var today = new Date();
	var ny = new Date(2023, 0, 1); //1st January 2023
	var one_day = 1000 * 60 * 60 * 24; //number of millisecond in 1 day

	var result = Math.round((ny - today) / one_day);

	alert("There are " + result + " days left until New Year");
</script>

<main>
	<div>
		<label>
			Name: <input type="text" name="UserName" bind:value={name} />
		</label>
	</div>
	<h1>Hello {name}!</h1>
	<p>
		Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
		how to build Svelte apps.
	</p>
	<p>There are {result} days left until New Year</p>
	<hr />
	<Example2 str="{name}" />
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
</style>
