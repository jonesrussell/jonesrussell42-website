<svelte:options immutable />

<script lang="ts">
	export let title: string;
	export let paragraph: string;
</script>

<h1 class="text-3xl text-blue-500 font-thin">{title}</h1>
<p class="mt-4 text-gray-700">{paragraph}</p>
