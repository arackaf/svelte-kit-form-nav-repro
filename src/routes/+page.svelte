<script>
  import { onMount } from "svelte";
  import SimpleForm from "./SimpleForm.svelte";

  onMount(() => {
    console.log("MOUNT");

    const portal = document.createElement("div");
    document.body.appendChild(portal);
    new SimpleForm({ target: portal });
  });
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

This one works: <SimpleForm />

This one does not, and causes a full re-render
