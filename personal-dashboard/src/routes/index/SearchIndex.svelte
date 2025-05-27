<script lang="ts">
	// implementing debounce
	let timeout: number;

	let search = function() {
		console.log('async operation here!');
	};

	function debounce(callback: () => void, duration: number) {
		clearTimeout(timeout);

		timeout = setTimeout(callback, duration);
	}

	// remove all 2 numbers from array

	let arr = [1, 2, 2, 2, 2, 8, 9, 10];

	for (let i = arr.length - 1; i >= 0; i--) {
		if(arr[i] === 2) {
			arr.splice(i, 1);
		}
	}

	console.log(arr)

</script>

<div class="flex items-center flex-col mt-6">
	<h1 class="text-3xl p-4 rounded-2xl font-bold bg-gradient-to-r from-amber-400 to-orange-500">Debounce in action</h1>
	<div class="mt-25 ">
		<input class="rounded-md border-b-gray-600" type="text" oninput={() => debounce(search, 1000)}
					 placeholder="Search" />
	</div>
</div>

