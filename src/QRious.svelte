<script>
    // npm i qrious

    import { onMount } from "svelte";
    import QRious from 'qrious';
    
    let canvas;

    export let value="";
    export let level="H";
    export let background="white";
    export let backgroundAlpha=1;
    export let foreground="black";
    export let foregroundAlpha=1;
    export let size=100;
    export let padding=null; // null means auto padding which CENTRES the QR Code!!!

    onMount(async () => {
        new QRious({
            level: level,
            element: canvas,
            background: background,
            backgroundAlpha: backgroundAlpha,
            foreground: foreground,
            foregroundAlpha: foregroundAlpha,
            size: size,
            padding: padding, 
            value: value
        })
    });

</script>

<svelte:element this="canvas" bind:this={canvas} {...$$props} />

