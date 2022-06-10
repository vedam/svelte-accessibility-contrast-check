<script>
	export let bg;
	export let color;

	$: txt_white = color === "--color-bg" ? true : false;
</script>

<div>
	<p class:txt_white style:background-color="var({bg})">
		Lorem ipsum dolor sit <span style:color="var({color})">adipicing</span>
		dimpedit reiciendis laudanum antium
		<span style:color="var({color})">iusto ratione</span>
		tempore.
	</p>
	<code>
		bg: {bg}<br />
		txt: {color}
	</code>
</div>

<style>
	div {
		margin: 0 0 6rem 1rem;
		width: 32rem;
	}

	span:hover {
		text-decoration: underline;
		cursor: pointer;
	}

	p {
		padding: 2.4rem;
		border-radius: var(--border-r);
	}

	.txt_white {
		color: var(--color-bg);
	}

	code {
		display: inline-block;
		margin: -1rem 0 0 0;
		line-height: 1.5;
		color: var(--);
	}
</style>
