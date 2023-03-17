<script>
    import { onMount } from 'svelte';
    import { select } from 'd3-selection';
    import textures from 'textures';

    let svgElem;

    const texture = textures
        .lines()
        .orientation('3/8', '7/8')
        .stroke('darkorange');

    onMount(() => {
        select(svgElem).call(texture);
    });
</script>

<main>
    <svg
        width="500"
        height="500"
        bind:this={svgElem}
    >
        <circle
            cx="250"
            cy="250"
            r="200"
            stroke="none"
            fill={texture.url()}
        />
    </svg>
</main>

<style>

</style>
