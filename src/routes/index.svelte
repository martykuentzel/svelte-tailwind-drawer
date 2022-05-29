<script>
  import Drawer from "$lib/ui/Drawer.svelte";

  let isOpen = false;
  const handleToggle = () => {
    isOpen = !isOpen;
  };
</script>

<Drawer {isOpen} on:clickAway={handleToggle}>
  <button class="m-12 text-bold text-xl" on:click={handleToggle}>Close</button>
</Drawer>

<div class="flex">
  <div class="m-auto">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="h-16 w-16 cursor-pointer duration-100 hover:scale-110"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
      stroke-width="2"
      on:click={handleToggle}
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        d="M4 6h16M4 12h16M4 18h16"
      />
    </svg>
  </div>
</div>
