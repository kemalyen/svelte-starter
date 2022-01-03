<script>
	import Container from 'sveltestrap/src/Container.svelte';
	import Navbar from '../components/Navbar.svelte';
	import Footer from '../components/Footer.svelte';

	let title = 'Admin';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<div class="sb-nav-fixed">
	<Navbar />
	<div id="layoutSidenav">
		<main>
			<Container fluid={true}>
				<slot />
			</Container>
		</main>
		<Footer />
	</div>
</div>
