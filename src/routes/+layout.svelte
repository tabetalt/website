<script lang="ts">
	import '@fontsource/poppins';
	import { serializeSchema } from '$lib/schema';
	import type { LocalBusiness, WithContext } from 'schema-dts';

	const localBusiness: WithContext<LocalBusiness> = {
		'@context': 'https://schema.org',
		'@type': 'LocalBusiness',
		name: 'Tabetalt AS',
		url: 'https://tabetalt.no',
		logo: 'https://tabetalt.no/logo.svg',
		image: 'https://tabetalt.no/logo.svg',
		description: 'Tabetalt is a software development company based in Oslo, Norway.',
		address: {
			'@type': 'PostalAddress',
			streetAddress: 'Myntgata 2',
			addressLocality: 'Oslo',
			postalCode: '0152',
			addressCountry: 'NO'
		},
		telephone: '+47 95 30 80 87'
	};
</script>

<svelte:head>
	{@html serializeSchema(localBusiness)}
</svelte:head>

<div class="container">
	<slot>
		<!-- +page.svelte is rendered here -->
	</slot>
</div>

<style>
	:global(:root) {
		--color-primary: #F47F5E;
    --color-background: #E9EBF1;
    --color-text: #000;
	}

	:global(body) {
		font-family: 'Poppins', sans-serif;
		background-color: var(--color-background);
		color: var(--color-text);
	}

	:global(a) {
		color: inherit;
		text-decoration: underline 0.15em rgba(0, 0, 0, 1);
		transition: text-decoration-color 300ms;
	}

	:global(a:hover) {
		text-decoration-color: rgba(0, 0, 0, 0);
	}

	.container {
		max-width: 800px;
		margin: 0 auto;

		padding: 1rem;
	}
</style>
