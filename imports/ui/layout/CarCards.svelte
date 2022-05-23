<script>
	import {onMount} from 'svelte';
	let carList = [];
	const url = 'https://car-data.p.rapidapi.com/cars?limit=10&page=0';
	const options = {
		method: 'GET',
		headers: {
			'X-RapidAPI-Host': 'car-data.p.rapidapi.com',
			'X-RapidAPI-Key': 'd949cb0134mshea1b89b5d430601p181634jsn50447f52519c'
		}
	};
	onMount(async function() {
			const response = await fetch(url, options);
			const data = await response.json();
			carList = data;
			console.log(carList);
		});
</script>

{#each carList as car}
	<!-- card -->
	<div class="m-2 flex w-96 flex-col justify-center bg-white rounded-2xl shadow-xl shadow-slate-300/60">
	  <!-- img -->
	  <img alt= "car frame" class="aspect-video w-96 rounded-t-2xl object-cover object-center" src="https://images.pexels.com/photos/3311574/pexels-photo-3311574.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" />
	  <!-- text information -->
	  <div class="p-4">
		 <small class="text-blue-400 text-xs">{car.make}</small>
		 <h1 class="text-2xl font-medium text-slate-600 pb-2">{car.model}</h1>
		 <p class="text-sm tracking-tight font-light text-slate-400 leading-6">Dodge is an American brand of automobiles and a division of Stellantis, based in Auburn Hills, Michigan..</p>
	  </div>
	</div>
{/each}

