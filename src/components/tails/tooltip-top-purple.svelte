<script lang="ts">
	let hover = false;

	function toggleHover() {
		hover = !hover;
	}
</script>

<div class="bg-white min-w-screen flex items-center justify-center">
	<div
		class="flex items-center relative text-gray-500 hover:text-gray-800 cursor-pointer"
		on:mouseenter={toggleHover}
		on:mouseleave={toggleHover}
	>
		<p>Hover Me</p>
		<div class="relative">
			<div
				class="absolute bg-purple-600 rounded-lg px-4 py-3 text-white w-64 inline-block bottom-0 mb-10 -ml-32"
				x-show="hover"
				x-transition:enter="transition ease-out duration-300"
				x-transition:enter-start="opacity-0 transform scale-90"
				x-transition:enter-end="opacity-100 transform scale-100"
				x-transition:leave="transition ease-in duration-300"
				x-transition:leave-start="opacity-100 transform scale-100"
				x-transition:leave-end="opacity-0 transform scale-90"
				x-cloak
			>
				<span class="leading-tight text-sm inline-block"
					>Hello, I'm a quick tooltip that you can drop into any project.</span
				>
				<span
					class="w-5 h-5 bg-purple-600 absolute right-0 bottom-0 -mb-1 transform rotate-45"
					style="left:50%;"
				/>
			</div>
			<svg
				class="w-4 h-4 ml-1"
				fill="none"
				stroke="currentColor"
				viewBox="0 0 24 24"
				xmlns="http://www.w3.org/2000/svg"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
				/>
			</svg>
		</div>
	</div>
</div>
