<script lang="ts">
  import SearchBar from './components/SearchBar.svelte'
  import Keybind from './components/Keybind.svelte'
  export let name: string
</script>

<main>
  <div class="row search-bar">
    <div class="cell">
      <SearchBar />
    </div>
  </div>
  <!-- <ul>
    <li>
      <Keybind shift>Alt</Keybind>
    </li>
    <li>
      <Keybind ctrl>w</Keybind>
    </li>
    <li>
      <Keybind>Windows</Keybind>
    </li>
    <li>
      <Keybind ctrl shift>Delete</Keybind>
    </li>
    <li>
      <Keybind />
    </li>
  </ul> -->
</main>

<style>
  main {
    padding: 1em;
    max-width: 500px;
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

  .search-bar {
    max-width: 500px;
    margin: 0 auto;
  }
</style>
