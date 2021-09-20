<script lang="ts">
  export let ctrl = false
  export let shift = false
</script>

<kbd
  >{#if ctrl}<kbd>Ctrl</kbd>+{/if}{#if shift}<kbd>Shift</kbd>+{/if}<kbd
    ><slot /></kbd
  ></kbd
>

<style>
  kbd {
    font: 1rem 'Consolas', 'Courier New', monospace;
    display: inline-block;
    background-color: #111;
    padding: 2px 4px;
    border-radius: 4px;
  }

  kbd > kbd {
    font-weight: 400;
  }
</style>
