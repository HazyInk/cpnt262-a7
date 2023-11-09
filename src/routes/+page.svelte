<script>
	import Card from "../lib/components/Card.svelte";
// const arr = ["one", "two", "three"]
// const obj = {src:'background.png', header:"TEST", paragraph:"TESTESTTESTTESTTEST"};
const obj = [
    { title: "Rainbow", content: "A dreamie rainbow background not your traditional rainbow as the pattern is slightly different but it gives a sense of wonder and warmth.", src:'background.png' },
    { title: "Clover", content: "A funny little sticker that resembles a shooting star but with the head of a clover instead of a star, wow what luck!", src:'clover.png' },
    { title: "Bushes", content: "Small landscape of some bushes, it was mostly just a practice piece that i thought looked nice.", src:'bushes.png' },
  ];
</script>


<div class="card-container">
  {#each obj as { title, content, src } (title)}
    <Card title={title} content={content} src={src} />
  {/each}
</div>

<style>
  .card-container {
    padding-top: 15rem;
    display: flex;
    justify-content: space-around; /* or space-between */
    flex-wrap: wrap;
    max-width: 1000px; /* Adjust as needed */
    margin: 0 auto; /* Center the cards */
  }
</style>