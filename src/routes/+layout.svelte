<script>
	import '../app.css';
	import Header from '../components/Header.svelte';
	import Drawer from '../components/Drawer.svelte';
	import Footer from '../components/Footer.svelte';
	import MockupWindow from '../components/MockupWindow.svelte';

	let { children } = $props();

	let drawerOpen = $state(false);

	const toggleDrawer = () => (drawerOpen = !drawerOpen);
</script>

<div class="flex min-h-screen flex-col">
	<!-- Header -->
	<Header {toggleDrawer} />

	<div class="flex flex-1">
		<!-- Sidebar drawer -->
		<Drawer {drawerOpen} {toggleDrawer} />

		<!-- Main content -->
		<main class="flex-1 p-4">
			{@render children()}
		</main>
	</div>

	<!-- Footer -->
	<Footer />
</div>
