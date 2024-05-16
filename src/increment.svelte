<script>
	import { count } from '$lib/stores';

	function increment() {
		count.update((/** @type {number} */ n) => n + 1);
	}
</script>

<button on:click={increment}> + </button>
