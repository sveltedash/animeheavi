<script>
    import SlowFloatCard from "./components/SlowFloatCard.svelte";
    import ToolTipButton from "./components/ToolTipButton.svelte";
</script>

<SlowFloatCard horizontal="true">
    <h1>Hello World</h1>
</SlowFloatCard>

<SlowFloatCard>
    <h1>Hello World</h1>
</SlowFloatCard>

<ToolTipButton title="Show ToolTip" on:click={() => window.alert("Hello World")} duration={1500}>
    This is a ToolTip!
</ToolTipButton>