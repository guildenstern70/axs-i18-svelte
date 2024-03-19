<script>
	import { _, locale } from 'svelte-i18n';
	import { get } from 'svelte/store';

	const changeLanguage = () => {
		const currentLocale = get(locale);
		if (currentLocale === 'en') {
			locale.set('it');
		} else {
			locale.set('en');
		}
	}

</script>

<h1>{$_('brevetti')}</h1>

<button on:click={changeLanguage}>{$_('cambia_lingua')}</button>
