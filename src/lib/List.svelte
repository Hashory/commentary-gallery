<script lang="ts">
  import Masonry from 'svelte-bricks'

  let nItems = 30
  $: items = [...Array(nItems).keys()]

  let [minColWidth, maxColWidth, gap] = [200, 800, 20]
  let width: number | undefined = undefined;
	let height: number | undefined = undefined;
</script>

<Masonry
  {items}
  {minColWidth}
  {maxColWidth}
  {gap}
  let:item
  bind:masonryWidth={width}
  bind:masonryHeight={height}
>
  <img src="" alt="aaa">
</Masonry>
