<script>
	let {current=$bindable(current), choices} = $props();
	
	// const properties = $props();
	// const choices = properties.choices;
	// let current = properties.current;

	function changeSelectedCity(newCity) {
		current = newCity;
	}
</script>

<div class="select">
	<nav>
		{#each choices as item}
			<a href="#{item}">{item}</a>
		{/each} 
		<!-- changeSelectedCity(item) -->
	</nav>
</div>

<style>
	.select {
		display: inline-block;
		border: 1px solid #666;
		padding: 10px;
	}
	a {
		display: inline-block;
		padding: 0px 10px;
	}
</style>