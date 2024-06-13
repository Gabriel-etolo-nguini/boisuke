<script>
  import Logo from '../assets/logo.png'

	import Beranda from "./gallery.svelte";
	import Profile from "./magazine.svelte";

	import Home from "../App.svelte";
	export let menu = 1;
</script>

<div class="nav">
<li><a href="/" on:click|preventDefault={() => (menu = 2)}><img src={Logo} class="logo" alt="Boisuke Logo" /></a></li> 
<ul id="menu">
	<li><a href="/" on:click|preventDefault={() => (menu = 1)}>Gallerie</a></li> 
  
	<li><a href="/" on:click|preventDefault={() => (menu = 3)}>A propos</a></li>
</ul>
</div>

{#if menu === 1}
<Beranda />
{:else if menu === 2}
<Home />
{:else if menu === 3}
<Profile />
{:else}
<h1>
	Page Not Found
</h1>
{/if}

<style>
ul{
  display : flex;
  padding: 0;
}
li{
		list-style: none;
    padding: 0rem 1rem 0rem 1rem;
	}
  .logo{height:10rem;}
  p{margin:0;}

.nav{display:flex; 
      flex-direction: column;
    align-items: center;
}
a{color:black;
font-family:"kenyanReg";
font-size: x-large;
}

</style>