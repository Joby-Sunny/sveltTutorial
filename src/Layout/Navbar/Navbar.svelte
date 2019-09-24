<script>
  import { Link } from "svelte-routing";
  export let Routes = [
    { path: "/admin", label: "Admin" },
    { path: "/", label: "Client" }
  ];
</script>

<ul id="nav-mobile" class="right hide-on-med-and-down">
  {#each Routes as route}
    <li>
      <Link to={route.path}>{route.label}</Link>
    </li>
  {/each}
</ul>
