<script>
	import { count } from '$lib/stores';
	import Increment from '../increment.svelte';
	import Decrement from '../decrement.svelte';
	import Reset from '../Reset.svelte';

	/**
	 * @type {any}
	 */
	let countValue;

	const unsubscribe = count.subscribe((value) => {
		countValue = value;
	});
</script>

<h1>The count is {countValue}</h1>

<Increment />
<Decrement />
<Reset />
