# Svelte Tailwind Drawer
A simple svelte Drawer component build with vanilla Tailwind

[Check out the demo](https://svelte.dev/repl/cecaf37f087541da80488480c7371b66?version=3.48.0)

Features
- Fully responsive
- Transitions
- Placement left or right
- Customizable max-screen-size
- Lock body scrolling when open
- and most importanly: very simple!

## Usage
No package bullshit - just copy paste the ~50 lines of `Drawer.svelte` code into your svelte project and you are fine :)
  
Call it via
```
<script>
  import Drawer from "$lib/ui/Drawer.svelte";

  let isOpen = false;
  const handleToggle = () => {
    isOpen = !isOpen;
  };
</script>

<Drawer {isOpen} on:clickAway={handleToggle}>
  <button class="m-12 text-bold text-xl" on:click={handleToggle}>Close</button>
  <!-- your stuff -->
</Drawer>
```

Open and Olose state must be handled via User. For easy usage propgate the state through your components via dispatcher. If the project gets more complicated I recommand handling the state via svelte stores.

## Build with

```
svelte: 3.44.0
tailwindcss: 3.0.24
```

## Parameters

| Parameter     | Default  | Description                                     |
|---------------|----------|-------------------------------------------------|
| isOpen        | false    | Two-way binding for open state of the component |
| placement     | right-0    | Side of screen to slide out from                |
| maxScreenSize | max-w-lg | Max Panel size (see [tailwindcss.com/docs/max-width](tailwindcss.com/docs/max-width)  |
