<script>
  import LoadingOverlay from "./LoadingOverlay.svelte";
  import { onMount } from 'svelte';

  onMount(() => {
    // Set padding for the body element
    document.body.style.padding = '0'; // Adjust the padding value as needed
  });
</script>

<style>

.app-container {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.iframe-container {
  position: relative;
  width: 100%;
  height: 100%;
}

/* Style the iframe itself */
.iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: none; /* Remove iframe border */
}

</style>

<div class="app-container">
  <LoadingOverlay />
  <div class="iframe-container">
	<iframe
	  title="dakubettergpt"
	  class="iframe"
	  src="https://plzdontcry-dakubettergpt.hf.space"
	  frameborder="0"
	  width="100%"
	  height="100%"
	></iframe>
  </div>
</div>
