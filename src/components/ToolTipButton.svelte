<script>
    import { fade } from "svelte/transition";

    let show = false;
    export let title = "Show Tooltip"
    export let duration = 1000;

    const toggleShow = () => {
        show = true;
        setTimeout(() => show = false, duration);
    }
</script>

<button on:mouseover={toggleShow} on:mouseleave={() => show = false} on:click>{title}</button>
{#if show}
    <p transition:fade><slot/></p>
{/if}

<style>
    button {
        margin: 0;
        padding: 15px;
        font-size: 20px;
        cursor: pointer;
        background-color: white;
        border: none;
        box-shadow: 0 10px 10px lightgray;
    }

    p {
        margin: 10px;
        padding: 10px;
        background-color: black;
        color: white;
        width: 10%;
        font-size: 15px;
        font-family: Consolas, monospace;
    }
</style>