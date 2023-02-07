<script>
  import Counter from "./lib/Counter.svelte";
</script>

<main>
  <div>
    <a
      href="https://protocol_stamps.arweave.dev"
      target="_blank"
      rel="noreferrer"
    >
      <img src="stamp-super-2.png" class="logo" alt="STAMP" />
    </a>
  </div>
  <h1>Stamp Protocol</h1>

  <div class="card">
    <Counter />
  </div>

  <p>
    Check out <a
      href="https://github.com/twilson63/stamp-protocol/tree/main/packages/stampjs"
      target="_blank"
      rel="noreferrer">StampJS</a
    >
  </p>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
