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

Type into the textboxes and hit enter

<hr />
<br />

This one works: <SimpleForm />

This one does not, and causes a full re-render
