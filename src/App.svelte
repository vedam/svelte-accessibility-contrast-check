<script>
	import "./assets/base.css";
	import "./assets/svelte-theme-default.css";
	import ColorBlock from "./lib/color-block.svelte";
	import CodeBlock from "./lib/code-block.svelte";
</script>

<main>
	<h1>Svelte Accessibility Contrast Check</h1>
	<h2>Text-links [passing lighthouse]</h2>
	<section>
		<ColorBlock color="--color-primary-text" bg="--color-bg" />
		<ColorBlock color="--color-primary-text" bg="--color-bg-light" />
		<ColorBlock color="--color-primary-text" bg="--color-bg-api" />

		<ColorBlock color="--color-secondary-text" bg="--color-bg" />
		<ColorBlock color="--color-secondary-text" bg="--color-bg-light" />
		<ColorBlock color="--color-secondary-text" bg="--color-bg-api" />

		<ColorBlock color="--color-accent-text" bg="--color-bg" />
		<ColorBlock color="--color-accent-text" bg="--color-bg-light" />
		<ColorBlock color="--color-accent-text" bg="--color-bg-api" />
	</section>

	<h2>Colored Boxes [passing lighthouse]</h2>
	<section>
		<ColorBlock color="--color-bg" bg="--color-primary-box" />
		<ColorBlock color="--color-bg" bg="--color-accent-box" />
		<ColorBlock color="--color-bg" bg="--color-secondary" />
	</section>

	<h2>Colored Boxes [--primary and --accent failing]</h2>
	<section>
		<ColorBlock color="--color-bg" bg="--color-primary" />
		<ColorBlock color="--color-bg" bg="--color-accent" />
		<ColorBlock color="--color-bg" bg="--color-secondary" />
	</section>

	<h2>Code blocks [passing lighthouse]</h2>
	<section>
		<CodeBlock style="background-color:var(--color-bg)" />
		<CodeBlock style="background-color:var(--color-bg-light)" />
		<CodeBlock style="background-color:var(--color-bg-api)" />
	</section>
</main>

<style>
	:root {
		font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
			Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
	}

	main {
		padding: 1em;
		margin: 0 auto;
	}

	section {
		display: flex;
		justify-content: center;
		flex-wrap: wrap;
	}

	h1,
	h2 {
		margin: 3rem 5rem;
		font-size: 3.6rem;
		font-weight: 400;
		text-align: left;
	}

	h2 {
		font-size: 2rem;
	}
</style>
