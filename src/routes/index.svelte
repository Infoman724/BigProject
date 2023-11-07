<script>
	import { stores } from '@sapper/app';
	const { session } = stores();
    import successkid from 'images/successkid.jpg'
</script>


<style>
	h1, figure, p {
		text-align: center;
		margin: 0 auto;
	}

	h1 {
		font-size: 2.8em;
		text-transform: uppercase;
		font-weight: 700;
		margin: 0 0 0.5em 0;
	}

	figure {
		margin: 0 0 1em 0;
	}

	img {
		width: 100%;
		max-width: 400px;
		margin: 0 0 1em 0;
	}

	p {
		margin: 1em auto;
	}

	@media (min-width: 480px) {
		h1 {
			font-size: 4em;
		}
	}
</style>

<svelte:head>
	<title>Svelte</title>
</svelte:head>

{#if $session.token}
	<h1>Добро пожаловать!</h1>
	<figure>
		<img alt="Success Kid" src="https://www.seekpng.com/png/detail/138-1387775_login-to-do-whatever-you-want-login-icon.png">
	</figure>
{:else}
	<h1>Всё работает корректно!</h1>
	<figure>
        <img alt="successkid" src="{successkid}">
	</figure>
{/if}