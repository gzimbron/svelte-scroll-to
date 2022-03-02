<header>
  <h1>
    ZimbronApps.com
    <span class="componente"> Scroll to Element </span>
  </h1>
  <div class="svelte">SvelteKit</div>
</header>
<slot />

<style>
  header {
    background: steelblue;
    color: white;
    text-align: center;
    padding: 5vh 20px;
    height: 150px;
  }
  h1 {
    font-family: 'Yanone Kaffeesatz', sans-serif;
    font-size: 2.5em;
    text-align: 'center';
    margin: 0;
    display: inline-block;
    letter-spacing: 1px;
  }
  h1 .componente {
    color: skyblue;
    font-size: 2rem;
    letter-spacing: 2px;
  }
  .svelte {
    position: absolute;
    bottom: 0;
    right: 0;
    font-size: 1.1rem;
    padding: 2px 5px;
    background: lightblue;
    color: steelblue;
  }
</style>
