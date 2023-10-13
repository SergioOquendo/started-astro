<!-- FILEPATH: /Users/sergioandresoquendo/Documents/Projects/started-astro/src/components/Card.svelte -->

<script>
  export let title = "";
  export let subtitle = "";
  export let imageSrc = "";
  export let buttonText = "";
  export let buttonLink = "";
</script>

<div class="bg-white rounded-lg shadow-lg overflow-hidden">
  <img
    class="w-full h-56 object-cover object-center"
    src={imageSrc}
    alt={title}
  />
  <div class="p-4">
    <h3 class="text-gray-900 font-medium text-lg mb-2">{title}</h3>
    <p class="text-gray-600 text-sm">{subtitle}</p>
  </div>
  {#if buttonText && buttonLink}
    <div class="flex items-center justify-end px-4 pb-4">
      <a
        href={buttonLink}
        class="bg-indigo-500 text-white font-medium py-2 px-4 hover:bg-indigo-600 transition duration-200 each-in-out rounded-full"
      >
        {buttonText}
      </a>
    </div>
  {/if}
</div>
