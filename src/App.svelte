<script>
  import Content from "./components/Content.svelte";
</script>

<main>
  <Content/>
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap');

  :global(*) {
    font-family: "inter";
  }

  :global(body) {
    background-color: rgb(35, 39, 46);
    color: rgb(245, 245, 245);
  }
</style>
