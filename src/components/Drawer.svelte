<script>
	export let drawerOpen = false;
	export let toggleDrawer;
</script>

<!-- Gabung class biasa dengan class binding -->
<div class={`drawer ${drawerOpen ? 'drawer-open' : ''}`}>
	<input id="my-drawer-2" type="checkbox" class="drawer-toggle" bind:checked={drawerOpen} />

	<!-- Sidebar -->
	<div class="drawer-side">
		<label for="my-drawer-2" aria-label="Close sidebar" class="drawer-overlay"></label>
		<ul class="menu bg-base-200 text-base-content min-h-full w-80 p-4">
			<li><a href="/">Sidebar Item 1</a></li>
			<li><a href="/profile">Sidebar Item 2</a></li>
		</ul>
	</div>
</div>
