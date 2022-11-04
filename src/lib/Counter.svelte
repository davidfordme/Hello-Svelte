<script>
  let count = 0
  const increment = () => {
    count += 1
  }

  $: doubled = count * 2;

  $: console.log('the count is ' + count);
</script>

<button on:click={ increment }>
  This button has been clicked {count} time{ (count !== 1)? 's' : ''}
</button>

<p>(...which doubled is {doubled})</p>

<style>
  p {
    font-size: 0.8rem;
  }
</style>