<script lang="ts">
	type Operator = '+' | '-' | '*' | '/';
	let num1 = 3;
	let num2 = 3;
	let op: Operator = '+';
	let result = 0;
	$: {
		if (op === '+') {
			result = num1 + num2;
		} else if (op === '-') {
			result = num1 - num2;
		} else if (op === '/') {
			result = num1 / num2;
		} else if (op === '*') {
			result = num1 * num2;
		}
	}
	function randomNumber() {
		num1 = Math.floor(Math.random() * 9999);
		num2 = Math.floor(Math.random() * 9999);
	}
</script>

<h1 class="text-4xl">Kalkulator</h1>
<input bind:value={num1} type="number" placeholder="0" />
<select bind:value={op}>
	<option>+</option>
	<option>-</option>
	<option>*</option>
	<option>/</option>
</select>
<input bind:value={num2} type="number" placeholder="0" />

<button on:click={randomNumber} class="bg-blue-800">Random</button>

<p>{num1}{op}{num2} = {result}</p>
