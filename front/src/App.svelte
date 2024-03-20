<script lang="ts">
  import { Router, Link, Route } from "svelte-routing";

  import Home from './routes/+page.svelte';
  import NotFound from './routes/+error.svelte';

  export let url = "";
</script>

<!-- https://github.com/EmilTholin/svelte-routing/issues/18 -->

<Router {url}>
  <nav>
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
    <Link to="/blog">Blog</Link>
  </nav>
  <div>
    <Route path="/"><Home /></Route>
    <Route><NotFound /></Route>
  </div>
</Router>
