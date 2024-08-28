<script>
	export let y;

	const tabs = [
		{ name: 'Projects', link: '#projects' },
		{ name: 'About', link: '#about' }
		// {name: 'Blog', '#blog'}
	];
</script>

<header>
	<h1>
		<b>Ljupcho</b> Baldovaliev
	</h1>
	<div class="">
		{#each tabs as tab, index}
			<a>
				<p>{tab.name}</p>
			</a>
		{/each}
	</div>
</header>
