<script lang="ts">
	import '../app.css';
	import SearchIndex from './index/SearchIndex.svelte';

	let { children } = $props();
</script>

<SearchIndex></SearchIndex>

{@render children()}
