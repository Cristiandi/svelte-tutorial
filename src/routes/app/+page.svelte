<script>
	import { fade } from 'svelte/transition';
	let visible = true;
</script>

<label>
	<input type="checkbox" bind:checked={visible} />
	visible
</label>

{#if visible}
	<p transition:fade={{ y: 200, duration: 2000 }}>
		Fades in and out
	</p>
{/if}
