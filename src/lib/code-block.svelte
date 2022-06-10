<script>
	export let style;
</script>

<div {style}>
	<code>
		<span class="function">&lt;script&gt;</span><br />
		<span class="comment"
			>&nbsp;&nbsp; // One of those informative comments<br />
		</span>
		<span class="keyword">&nbsp;&nbsp; import </span>
		Nested
		<span class="keyword"> from</span>
		<span class="string"> './Nested.svelte'</span>;<br />
		<span class="keyword">&nbsp;&nbsp; let </span>
		unused_string =
		<span class="template-string">`A template string`</span>;<br />
		<br />
		<span class="function">&lt;/script&gt;</span><br />
		<br />
		<span class="function">&lt;p&gt;</span>These styles...<span class="function"
			>&lt;/p&gt;</span
		><br />
		<span class="function">&lt;Nested /&gt;</span><br />
		<br />
		<span class="function">&lt;style&gt;</span><br />
		<span class="function">&nbsp;&nbsp;p</span>
		{"{"}<br />
		&nbsp;&nbsp;&nbsp;&nbsp;color:
		<span class="keyword"> purple</span>;<br />
		&nbsp;&nbsp;&nbsp;&nbsp;font-family:
		<span class="string"> 'Comic Sans MS'</span>, cursive;<br />
		&nbsp;&nbsp;&nbsp;&nbsp;font-size:
		<span class="number"> 2em</span>;<br />
		&nbsp;&nbsp;{"}"}<br />
		<span class="function">&lt;/style&gt;</span><br />
	</code>
</div>

<style>
	div {
		padding: 3rem 3.5rem;
		margin: -1rem 0 0 0;
		border-radius: var(--border-r);
	}

	code {
		display: block;
		line-height: 1.5;
		color: var(--color-code-base);
		mix-blend-mode: multiply;
	}

	.comment {
		color: var(--color-code-comment);
	}

	.keyword {
		color: var(--color-code-keyword);
	}

	.function {
		color: var(--color-code-function);
	}

	.string {
		color: var(--color-code-string);
	}

	.number {
		color: var(--color-code-number);
	}

	.template-string {
		color: var(--color-code-template-string);
	}
</style>
