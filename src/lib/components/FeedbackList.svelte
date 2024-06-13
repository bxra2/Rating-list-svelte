<script>
  import FeedbackItem from "./FeedbackItem.svelte";
  import { FeedbackStore } from "../../stores";
  import { fade, scale } from "svelte/transition";
</script>

{#each $FeedbackStore as f (f.id)}
  <div in:scale out:scale={{ duration: 300 }}>
    <FeedbackItem item={f} />
  </div>
{/each}
