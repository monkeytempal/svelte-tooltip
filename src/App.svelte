<script>
  import { tooltip } from './components/tooltip.js'

  export let name
</script>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
  <p>
    This is a tooltip created for svelte. Please hover over <span
      use:tooltip
      data-tooltip="Welcome to the svelte tooltip repo.">THIS TEXT</span
    > to see a tooltip.
  </p>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  /* Tooltip */
  :global([data-tooltip]) {
    display: inline-block;
    position: relative;

    /* Just for demo */
    font-weight: bold;
    color: teal;
  }
</style>
