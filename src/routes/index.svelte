<script>
  let now = new Date()
  
  $: seconds = now.getSeconds()
  $: minutes = now.getMinutes()
  $: hours = now.getHours()

  setInterval(() => {
      now = new Date()
    }, 1000)
</script>
<style type='text/scss'>
  .seconds {
    color: red;
  }

  h1 {
    font-family: monospace;
    margin: 0 auto;
    display: block;
    width: max-content;
  }
  
</style>

<svelte:head>
	<title>Steven's project</title>
</svelte:head>

<h1>
  We're living at {hours}:<span class:minutes={minutes % 5 == 0}>{minutes}</span>:<span class:seconds={seconds % 5 == 0}>{seconds}</span>
</h1>
