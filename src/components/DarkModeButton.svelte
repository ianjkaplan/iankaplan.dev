<script lang="ts">
    import { isDarkMode } from "../stores";
    import Button from "@smui/button";
    import { onMount } from "svelte";

    let darkText: boolean | undefined = undefined;
    // set is darkmode to whatever the media query returns
    onMount(() => {
        darkText = window.matchMedia("(prefers-color-scheme: dark)").matches;
        isDarkMode.update(() => darkText);
    });

    const toggleDarkMode = () => {
        darkText = !darkText;
        isDarkMode.update(() => darkText);
    };
</script>

<Button on:click={toggleDarkMode} variant="outlined">
    {darkText ? "Light" : "Dark"}
</Button>
