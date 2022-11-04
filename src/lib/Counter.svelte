<script>
  export let count = 0
  export let shouldShowDouble = false
  const increment = () => {
    count += 1
  }

  // '$:' is a variable or method that will update when a variable defined inside updates
  $: doubled = count * 2;
  $: {
    console.log('the count is ' + count);
  }
</script>

<button on:click={ increment }>
  This button has been clicked {count} time{ (count !== 1)? 's' : ''}
</button>

<!-- https://svelte.dev/tutorial/if-blocks -->
{#if shouldShowDouble }
  <p>(...which doubled is {doubled})</p>
{/if}

<style>
  p {
    font-size: 0.8rem;
  }
</style>