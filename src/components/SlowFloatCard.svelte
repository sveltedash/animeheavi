<script>
    export let horizontal = false;
</script>

<div class={horizontal ? "card-horizontal" : "card"}>
    <slot/>
</div>

<style>
    @keyframes slow-float-vertical {
        50% { transform: translateY(20px); box-shadow: 0 -10px 10px lightgray }
    }

    @keyframes slow-float-horizontal {
        50% { transform: translateX(20px); box-shadow: -10px 0 10px lightgray }
    }

    .card {
        margin: 10px;
        padding: 10px;
        box-shadow: 0 10px 10px lightgray;
        font-family: Consolas, monospace;
        text-align: center;
        animation: slow-float-vertical 4s ease-in-out infinite;
    }

    .card-horizontal {
        margin: 10px;
        padding: 10px;
        box-shadow: 10px 0 10px lightgray;
        font-family: Consolas, monospace;
        text-align: center;
        animation: slow-float-horizontal 4s ease-in-out infinite;
    }

    @media screen and (min-width: 760px) {
        .card, .card-horizontal {
            width: 25%;
            margin: 10px auto;
        }
    }
</style>