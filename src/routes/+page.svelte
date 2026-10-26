<script>
	import Quote from "#lib/components/Quote.svelte";
</script>

<main class="min-h-screen bg-[#faf9f6] px-6 py-20">
	<div class="mx-auto max-w-2xl">
		<header class="mb-16">
			<p class="text-xs tracking-[0.25em] text-stone-400 uppercase">Zitatsammlung</p>
			<h1 class="mt-4 font-['Instrument_Serif'] text-6xl leading-none text-stone-900 sm:text-7xl">
				Data <i class="text-[#c0603a]">Exchange</i>
			</h1>
			<p class="mt-5 max-w-sm text-stone-500">Sieben Sätze, die bleiben. Zum Lesen, Kopieren und Teilen.</p>
		</header>

		<Quote author="Abraham Lincoln">
			My dream is of a place and a time where America will once again be seen as the last best hope of earth.
		</Quote>

		<Quote author="Oscar Wilde">
			<p>Be yourself; everyone else is already taken.</p>
		</Quote>

		<Quote author="Albert Einstein">
			<p>Life is like riding a bicycle. To keep your balance, you must keep moving.</p>
		</Quote>

		<Quote author="Steve Jobs">
			<p>Stay hungry, stay foolish.</p>
		</Quote>

		<Quote author="Nelson Mandela">
			<p>It always seems impossible until it's done.</p>
		</Quote>

		<Quote author="Mahatma Gandhi">
			<p>Be the change that you wish to see in the world.</p>
		</Quote>

		<Quote author="Confucius">
			<p>It does not matter how slowly you go as long as you do not stop.</p>
		</Quote>

		<footer class="border-t border-stone-200 pt-8 text-center font-['Instrument_Serif'] text-xl text-stone-400 italic">
			Ende.
		</footer>
	</div>
</main>