<script>
	import Logo from './components/logo.svelte';
</script>

<div class="logo-container">
	<div class="logo">
		<Logo />
	</div>
	<p>Organisasjonsnummer: 920 654 517</p>
</div>

<style>
	.logo-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		margin: 2rem 0;
	}

	.logo {
		width: 200px;
	}
</style>
