<script lang="ts">
    import { onMount } from "svelte";
    import { isDarkMode } from "../stores";
</script>

<svelte:head>
    <title>Ian Kaplan</title>
    <!--- toggle dark theme-->
    {#if $isDarkMode}
        <link
            rel="stylesheet"
            href="/smui.css"
            media="(prefers-color-scheme: light)"
        />
        <link
            rel="stylesheet"
            href="/smui-dark.css"
            media="screen and (prefers-color-scheme: dark)"
        />
    {:else}
        <link rel="stylesheet" href="/smui.css" />
    {/if}
</svelte:head>

<main class="container">
    <slot />
</main>

<div class="footer">
    <em>
        This site is built with Svelte! See <a href="https://kit.svelte.dev"
            >kit.svelte.dev</a
        > to read the documentation
    </em>
</div>

<style>
    main.container {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        width: 80vw;
        margin: auto;
    }

    .footer {
        position: fixed;
        left: 0;
        bottom: 0;
        width: 100%;
        text-align: center;
        margin-bottom: 1rem;
        font-size: 0.8rem;
    }
</style>
