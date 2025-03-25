<script>
	import CityPicker from './CityPicker.svelte';
	import CityDetails from './CityDetails.svelte';
	import cityInfo from './cityinfo.json'

	let selectedCity = $state("Boston");
	
	const cityNames = cityInfo.map(city => city.name);
	const selectedDetails = $derived(cityInfo.find(city => city.name == selectedCity));
</script>

<div class="select">
	<h1>City Explorer -> </h1>
	<CityPicker bind:current={selectedCity} choices={cityNames} />
	<CityDetails info={selectedDetails} />
</div>

<style>
	h1 {
		color: lightsteelblue;
	}
</style>