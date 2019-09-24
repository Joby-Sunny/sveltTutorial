<script>
  import "../node_modules/materialize-css/dist/css/materialize.min.css";
  import "../node_modules/materialize-css/dist/js/materialize.min.js";
  import { Router, Route } from "svelte-routing";
  import Header from "./Layout/Header/Header.svelte";
  import Admin from "./Pages/Admin/Admin.svelte";
  import Home from "./Pages/Home/Home.svelte";
  export let Routes = [
    { path: "/admin", component: Admin },
    { path: "/", component: Home }
  ];
</script>

<style>

</style>

<Router>
  <Header />
  <div class="container">
    {#each Routes as route}
      <Route path={route.path} component={route.component} />
    {/each}
  </div>
</Router>
