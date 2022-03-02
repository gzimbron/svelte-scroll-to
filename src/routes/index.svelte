<script>
  import { element } from 'svelte/internal';

  const scrollToElement = (selector) => {
    const elemento = document.querySelector(selector);
    if (!elemento) return;

    let posicion = elemento.getBoundingClientRect().top;
    let offset = posicion + window.pageYOffset;

    window.scrollTo({
      top: offset,
      behavior: 'smooth',
    });
  };
</script>

<ul>
  <li>
    <a href={'#'} on:click|preventDefault={() => scrollToElement('#seccion1')}
      >Secc 1</a
    >
  </li>
  <li>
    <a href={'#'} on:click|preventDefault={() => scrollToElement('#seccion2')}
      >Secc 2</a
    >
  </li>
  <li>
    <a href={'#'} on:click|preventDefault={() => scrollToElement('#seccion3')}
      >Secc 3</a
    >
  </li>
</ul>

<div class="spacer" />
<div class="spacer" />
<div class="spacer" />
<div id="seccion1"><h1>Seccion 1</h1></div>
<div class="spacer" />
<div class="spacer" />
<div class="spacer" />
<div id="seccion2"><h1>Seccion 2</h1></div>
<div class="spacer" />
<div class="spacer" />
<div class="spacer" />
<div id="seccion3"><h1>Seccion 3</h1></div>

<style>
  ul {
    display: flex;
    justify-content: space-evenly;
  }

  li {
    list-style: none;
    padding: 0;
    width: 100px;
    height: 30px;
  }

  .spacer {
    height: 500px;
  }
  h1 {
    background: grey;
    color: white;
  }
</style>
