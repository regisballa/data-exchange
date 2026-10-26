<script>
    let { children, author = "Not known" } = $props();
    let quote;

    async function copy() {
        await navigator.clipboard.writeText(quote.textContent.trim());
        let permission = Notification.permission;
        if (permission !== "granted") {
            permission = await Notification.requestPermission();
        }
        if (permission === "granted") {
            new Notification("Quote copied", {
                body: "You successfully copied the quote to your clipboard.",
            });
        }
    }

    async function share() {
        await navigator.share({
            title: 'Please read this quote',
            text: quote.textContent.trim(),
        });
    }
</script>

<article class="group border-t border-stone-200 py-12">
    <span class="block h-8 font-['Instrument_Serif'] text-7xl leading-none text-[#c0603a]">“</span>

    <blockquote bind:this={quote} class="font-['Instrument_Serif'] text-3xl leading-snug text-stone-700 transition group-hover:text-stone-950 sm:text-4xl">
        {@render children?.()}
    </blockquote>

    <div class="mt-6 flex items-center justify-between text-sm">
        <p class="flex items-center gap-3 text-stone-500">
            <span class="h-px w-6 bg-stone-400"></span>
            {author}
        </p>

        <div class="flex gap-2">
            <button class="cursor-pointer rounded-full px-3 py-1 text-stone-500 hover:bg-stone-200/70 hover:text-stone-900" onclick={copy}>Kopieren</button>
            <button class="cursor-pointer rounded-full px-3 py-1 text-stone-500 hover:bg-stone-200/70 hover:text-stone-900" onclick={share}>Teilen</button>
        </div>
    </div>
</article>