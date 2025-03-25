<script>
	const properties = $props();
	const info = properties.info;
	const name = info.name;
	const sights = info.topSites;
</script>

<div class="details">
	<h3><i>Welcome to {name}!</i></h3>
	<p>You should visit:</p>
	{#each sights as item}
		<ul><li>{item}</li></ul>
	{/each}
</div>

<style>
	.details {
		background-color: #ccc;
		padding: 15px;
	}
</style>