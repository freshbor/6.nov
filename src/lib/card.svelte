<script lang="ts">
	export let name: string;
	export let slika: string;
	export let description: string;
</script>

<div class="p-5 rounded-2xl border-4 border-black bg-gradient-to-r from-green-600 to-purple-700">
	<h4 class="text-3xl">{name.toUpperCase()}</h4>

	<p>{description}</p>
	<button class="bg-red-950 hover:bg-blue-900 text-white rounded-xl p-2">Preberi več</button>
</div>
