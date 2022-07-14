<script>
	import '/src/styles/app.scss'
	import Header from '../lib/Header.svelte'

	let title = 'Fluffy Cuddles'
	let description = 'Furry cookie clicker but you give pets and cuddles uwu'
</script>

<svelte:head>
	<title>{title}</title>
	<meta name="description" content={description} />
	<meta property="og:type" content="website" />
	<!-- <meta property="og:image" content="https://raw.githubusercontent.com/FurryCookie/FurryCookie/master/assets/img/logo.png" /> -->
	<meta property="og:site_name" content={title} />
	<meta property="og:title" content={title} />
	<meta property="og:description" content={description} />
	<!-- <meta name="twitter:image" content="https://raw.githubusercontent.com/FurryCookie/FurryCookie/master/assets/img/logo.png" /> -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content={title} />
	<meta name="twitter:description" content={description} />
</svelte:head>

<Header />
<main>
	<slot />
</main>
