<script>
	import { fade } from 'svelte/transition';
	let { children } = $props();
</script>

<div class="grid h-screen w-full grid-cols-[300px_1fr] grid-rows-[50px_1fr] border">
	<div class="border">1</div>
	<div class="border">2</div>
	<div class="border">3</div>
	<div class="border">
		<div in:fade={{ duration: 1000 }}>
			{@render children()}
		</div>
	</div>
</div>
