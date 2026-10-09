<script lang="ts">
    import { onMount } from 'svelte'
	import init, {addition, type InitOutput} from 'ita-web'
    let initOutput: InitOutput;
    onMount(async () => {
        initOutput = await init()
    })
</script>

{#if initOutput}
    <h1>{addition(1, 2)}</h1>
{/if}

<style>
</style>