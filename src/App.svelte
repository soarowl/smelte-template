<script>
  import { Button, Switch, Snackbar } from "smelte";
  import Header from "./Header.svelte";

  export let name;

  let showSnackbar = false;
</script>

<Header />
<div class="container mx-auto h-full items-center">
  <h1>Hello {name}!</h1>
  <h2>Hello {name}!</h2>
  <h3>Hello {name}!</h3>
  <h4>Hello {name}!</h4>
  <h5>Hello {name}!</h5>
  <h6>Hello {name}!</h6>
  <div class="py-6">
    <Button>Button</Button>
  </div>
  <div class="py-6">
    <Switch label="Switch" />
  </div>

  <Button on:click={() => (showSnackbar = true)}>Show snackbar</Button>

  <Snackbar bind:value={showSnackbar}>
    <div>Have a nice day.</div>
    <div slot="action">
      <Button text on:click={() => (showSnackbar = false)}>Dismiss</Button>
    </div>
  </Snackbar>
</div>
