<script lang="ts">
	let hover = false;
</script>

<div class="flex justify-center items-center min-w-screen bg-white">
	<a
		on:mouseenter={() => {
			hover = true;
		}}
		on:mouseleave={() => {
			hover = false;
		}}
		href="https://www.google.com"
		class="relative inline-block font-medium text-indigo-500 text-base"
	>
		<span class="block">Link Underline Animation</span>
		<span class="absolute left-0 bottom-0 h-1 -mb-1 inline-block w-full overflow-hidden">
			<span
				x-show="hover"
				class="absolute inset-0 h-1 border-t-2 border-indigo-500 inline-block h-full w-full transform"
				x-transition:enter="transition ease-out duration-300"
				x-transition:enter-start="-translate-x-full"
				x-transition:enter-end="translate-x-0"
				x-transition:leave="transition ease-out duration-300"
				x-transition:leave-start="translate-x-0"
				x-transition:leave-end="translate-x-full"
			/>
		</span>
	</a>
</div>
