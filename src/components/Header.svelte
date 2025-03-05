<script>
	export let y;

	const tabs = [
		{ name: 'Projects', link: '#projects' },
		{ name: 'About', link: '#about' }
		// {name: 'Blog', '#blog'}
	];
</script>

<header class="h-full align-middle">
	<h1>
		Ljupcho Baldovaliev
	</h1>
	<div class="">
		{#each tabs as tab, index}
			<a>
				<p>{tab.name}</p>
			</a>
		{/each}
	</div>

	<img src="/assets/smile.png" class="size-1/5 p-6 rounded-full border-2 backdrop-blur bg-amber-50" alt="avatar"/>
</header>
