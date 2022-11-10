<script lang="ts">
    import { onMount } from "svelte";
	import { identity } from "svelte/internal";
    import { loadFull } from "tsparticles";

    import { initID } from "$lib/_particlesInternalStore";

    export let id: number = 0;
    export let limit: number = 60;

    let ParticlesComponent: any;

    onMount(async () => {
        const module = await import("svelte-particles");

        ParticlesComponent = module.default;
    });

    let particlesConfig = {
        fpsLimit: 30,
        fullScreen: false,
        particles: {
            number: {
                limit: limit
            },
            color: {
                value: "#111827"
            },
            links: {
                enable: true,
                color: "#d1d5db",
            },
            move: {
                enable: true,
                speed: 1
            },
        },
    };

    let particlesInit = async (main: any) => {
        if ($initID == -1)
            $initID = id;
            
        if (id === $initID)
            await loadFull(main);
    };
</script>

<style>
    :global([id^="tsparticles-"]) {
        height: 100%;
    }
</style>

<svelte:component
    this="{ParticlesComponent}"
    id={"tsparticles-" + id}
    options="{particlesConfig}"
    particlesInit="{particlesInit}"
/>