<script context="module">
  import {page} from '$app/stores'
</script>

<script>
  export let blogTitle = 'Kerngesund'

  let path
  $: ({pathname} = $page)
</script>

<header>
  <nav>
    <ul>
      <li><a data-selected={pathname === '/'} href="/">Startseite</a></li>
    </ul>
  </nav>
  <span>{blogTitle}</span>
</header>

<style>
  ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  a[data-selected='true'] {
    font-weight: 600;
    color: #555;
  }
  a {
    text-decoration: none;
    display: block;
    color: black
  }

  header {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start;
    margin: 1em;
    padding-bottom: .5em;
    border-bottom: 1px solid #ededed;
  }
  header span {
    background-color: #f71070;
    color: white;
    font-weight: bold;
    padding: .35rem .5rem;
  }
  @media screen and (min-width: 400px) {
    header {
      flex-direction: row-reverse;
      align-items: center;
    }
  }
</style>
