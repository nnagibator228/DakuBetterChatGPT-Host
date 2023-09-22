<script>
  import { afterUpdate, beforeUpdate } from "svelte";
  import { fade } from "svelte/transition";
  import Image from "./Image.svelte";
  export let delay = 3500;

  let showOverlay = true;

  afterUpdate(() => {
    setTimeout(() => {
      showOverlay = false;
    }, delay);
  });

</script>

<style>
  .loading-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 1);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 999;
  }

</style>

{#if showOverlay}
<div class="loading-overlay" transition:fade >
  <Image src="./loading.gif" />
</div>
{/if}
