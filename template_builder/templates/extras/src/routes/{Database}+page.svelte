<script lang="ts">
	import NextStep from '$lib/components/NextStep.svelte';
</script>

<main>
	<img src="/favicon.png" width="128px" alt="o7 Logo" />
	<h1>Welcome to the o7 stack!</h1>
	<h2>Next Steps:</h2>
	<div class="steps">
		<NextStep
			title="Edit this page"
			learnMore="https://svelte.dev/tutorial/basics"
		>
			<p>
				Edit <code class="lime">src/routes/+page.svelte</code> to see your changes
				live.
			</p>
			<p>
				The source for these cards is in <code class="lime"
					>src/lib/components/NextStep.svelte</code
				>.
			</p>
			<p>
				There's some global styling in <code class="lime">src/app.css</code>.
			</p>
		</NextStep>
		<NextStep
			title="Work on your database schema"
			learnMore="https://www.prisma.io/docs/concepts/components/prisma-schema"
		>
			<p>
				Write a Prisma schema in <code class="red">prisma/schema.prisma</code>.
			</p>
			<p>
				Run <code class="red">pnpm db:push</code> to update your database typings.
			</p>
			<p>
				Remember that you're using <a
					href="https://github.com/kysely-org/kysely"
					target="_blank">Kysely</a
				>
				instead of Prisma to make your queries, and
				<code class="red">import {'{ db }'} from '$lib/db'</code>!
			</p>
		</NextStep>
	</div>
</main>

<style>
	main {
		display: flex;
		height: 100vh;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	h1 {
		font-size: 1.875rem;
		line-height: 2.25rem;
		font-weight: 700;
	}
	h2 {
		margin-top: 1.5rem;
		margin-bottom: 1.5rem;
		font-size: 1.5rem;
		line-height: 2rem;
	}
	a {
		color: rgb(96 165 250);
	}
	a:hover {
		text-decoration: underline;
	}
	.steps {
		display: flex;
		justify-content: center;
		max-width: 64rem;
		gap: 1rem;
		padding: 0 0.75rem;
	}
	.lime {
		color: rgb(190 242 100);
	}
	.red {
		color: rgb(252 165 165);
	}
	code {
		background: rgb(24 24 27);
		padding: 0.125rem;
	}
</style>
