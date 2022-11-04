<script>
  let count = 0
  const increment = () => {
    count += 1
  }
</script>

<button on:click={ increment }>
  This button has been clicked {count} time{ (count !== 1)? 's' : ''}
</button>
