<script>
  import AuthorCard from '$lib/AuthorCard.svelte'
  import PostsGrid from '$lib/PostsGrid.svelte'

  export let posts
  export let authors
</script>

<svelte:head>
  <title>Kerngesund</title>
</svelte:head>

<h1>Kerngesund</h1>

<PostsGrid {posts} />

<h2 style="margin-top: 4rem; margin-bottom: 1rem;">Autor{authors.length > 1 ? 's' : ''}</h2>

{#each authors as author}
  <AuthorCard {author} />
{/each}
