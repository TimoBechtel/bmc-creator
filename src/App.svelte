<svelte:head>
  <title>{heading || 'Business Model Canvas Creator'}</title>
</svelte:head>

<header>
  <h1
    contenteditable="true"
    on:input={e => {
      heading = e.target.innerHTML;
    }}>
    Business Model Canvas Creator
  </h1>
  <p>
    Just edit the texts and print when you're done. You can also edit the
    heading.
    <br />
    For printing, set scaling to 55% and format to landscape in your printer
    settings.
  </p>
  <a href="https://github.com/TimoBechtel/bmc-creator">Github</a>
</header>
<main>
  <Canvas />
</main>

<script>
  import Canvas from './components/Canvas.svelte';

  let heading = '';
</script>

<style lang="scss">
  header {
    padding: 20px;
    h1 {
      outline: none;
    }
  }
  @media print {
    header {
      margin: 0;
      padding: 0;
      p,
      a {
        display: none;
      }
    }
  }
</style>
