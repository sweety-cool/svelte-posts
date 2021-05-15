<script>
	import faker from "faker";
	import Post from "./Post.svelte";

	let posts = [];

	function gen() {
		// loop and generate
		for (let i = 0; i < 50; i++) {
			// Generate
			const username = faker.name.findName();
			const image = `https://robohash.org/${encodeURI(
				username
			)}.png?set=set4`;
			const likes = Math.round(Math.random() * 1000);
			const comments = Math.round(Math.random() * 1000);

			// Add to array
			posts.push({ username, image, likes, comments });
		}
		// copy old array as new array to old variable (for updating svelte)
		posts = [...posts];
	}

	gen();
</script>

<div class="posts">
	{#each posts as p}
		<Post data={p} />
	{/each}
</div>

<style>
	.posts {
		max-width: 30rem;
		margin: auto;
	}
</style>
