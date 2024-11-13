<script lang="ts">
	import { page } from '$app/stores';
	import '../app.css';
	function bold(link: string) {
		if (link === $page.url.pathname) {
			return 'font-bold';
		} else {
			return '';
		}
	}
</script>

<nav class="w-full p-6 bg-red-400 bg-gradient-to-red-700">
	<a href="/" class={$page.url.pathname === '/' ? 'font-bold' : ''}>gumb</a>
	<a href="/domov" class={$page.url.pathname === '/' ? 'font-bold' : ''}>domov</a>
	<a href="/trgovina" class={$page.url.pathname === '/' ? 'font-bold' : ''}>trgovina</a>
	<a href="/kalkulator" class={$page.url.pathname === '/' ? 'font-bold' : ''}> kalkulator</a>
</nav>
<div class="w-full h-screen bg-blue-900">
	<slot />
</div>
