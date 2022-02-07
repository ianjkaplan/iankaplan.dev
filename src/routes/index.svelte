<script context="module" lang="ts">
    import DarkModeButton from "../components/DarkModeButton.svelte";
    export const prerender = true;
</script>

<div style="align-self: flex-end;">
    <DarkModeButton />
</div>
<h1>Ian Kaplan</h1>
<div class="flex-row">
    <div>
        <p>CTO of Hybrid Performance Method</p>
    </div>

    <div class="headshot">
        <img src="/headshot.jpeg" alt="Ian Kaplan Headshot" />
    </div>
</div>

<style>
    .flex-row {
        display: flex;
        direction: row;
        align-items: flex-start;
        justify-content: space-around;
        width: 100%;
    }
    .headshot {
        width: 100px;
        height: 100px;
        position: relative;
        overflow: hidden;
        border-radius: 50%;
    }
    img {
        display: inline;
        margin: 0 auto;
        height: 100%;
        object-position: -38px 0;
    }
</style>
