<script lang="ts">
  let query = ''

  const handleKeypress = (e) => {
    console.log(e.keyCode)
    if (e.keyCode === 13) {
      window.location = `https://duckduckgo.com/?q=${query}`
    }
  }
</script>

<div>
  <input
    type="text"
    placeholder="Поисковый запрос или адрес"
    bind:value={query}
    on:keypress={handleKeypress}
  />
  <ul
    class="suggestions"
    class:hidden={true || query == null || query.length === 0}
  >
    <li><a href="">Google</a></li>
    <li><a href="">Youtube</a></li>
    <li><a href="" class="selected">Google</a></li>
    <li><a href="">Youtube</a></li>
    <li><a href="">Google</a></li>
    <li><a href="">Youtube</a></li>
  </ul>
</div>

<style>
  div {
    position: relative;
    margin: 20px;
  }

  input {
    display: block;
    width: 100%;
  }

  .suggestions {
    position: absolute;
    top: calc(100% + 10px);
    /* top: 100%; */
    left: -10px;
    right: -10px;
    z-index: 10;
    background-color: var(--bg);

    border: 1px solid var(--faded-2);
    box-shadow: 0 0 8px #000;
    list-style: none;
  }

  a {
    display: block;
    line-height: 40px;
    font-size: 20px;
    color: var(--text);
    padding-left: 20px;
  }

  a:hover {
    background-color: var(--faded-3);
  }

  a:focus {
    background-color: var(--faded-2);
    outline: 1px solid var(--text);
  }
</style>
