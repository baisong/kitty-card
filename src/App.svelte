<script>
	export let name;
	export let entryTitle = "Lorem ipsum dolor sit amet, consectetur adi piscing elit sedconsectetur, justo non finibus";
	export let entryDate = "January 25, 2019";
	export let entryBody = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam luctus justo at urnavolutpat, eu fringilla mi malesuada. Quisque purus purus, pellentesque sed fermentumac, egestas ac mi. Aliquam erat volutpat.";
</script>

<main>
	<div class="responsive-card">
		<div class="card-media">
			<div class="overlay">
				<span class="entry-date">{entryDate}</span>
				<div class="flourish"></div>
			</div>
		</div>
		<div class="card-body">
			<div class="entry-wrapper">
				<h3 class="entry-title">{entryTitle}</h3>
				<ul class="entry-meta">
					<li class="meta-author-source">
						<p>Author Name, via <a href="#">Source</a></p>
					</li>
					<li class="meta-resource-type">
						<p><a href="#">Resource Type</a></p>
					</li>
				</ul>
				<div class="entry-body">{entryBody}</div>
			</div>
		</div>
	</div>
</main>

<style>
	:root {
		font-family: 'Helvetica Neue', HelveticaNeue, Arial, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', sans-serif;
		--kitty-blue: #0275d8;
		--dark-gray: #373a3c;
		--light-gray: #e5e5e5;
		--bright-yellow: #fff24d;
		--bright-yellow-transparent: #fff24d00;
	}
	.responsive-card {
		border: 1px solid var(--light-gray);
		color: var(--dark-gray);
		border-radius: 0.25em;
	}
	.responsive-card .card-body {
		padding: 0 1em 1em;
	}
	.responsive-card a,
	.responsive-card .entry-title {
		color: var(--kitty-blue);
	}
	.responsive-card .entry-title {
		font-weight: bold;
		margin: 0.75em 0;
	}
	.responsive-card .entry-date {
		background: var(--kitty-blue);
		color: white;
		text-transform: uppercase;
	}
	.responsive-card {
		display: flex;
	}
	.responsive-card .card-media {
		min-width: 170px;
	}
	.responsive-card .entry-meta {
		display: flex;
		font-size: 0.9em;
		padding: 0;
	}
	.responsive-card .entry-meta li:first-of-type {
		list-style-type: none;
	}
	.responsive-card .entry-meta li + li {
		list-style-type: disc;
		margin-left: 2em;
	}
	.responsive-card .entry-meta p {
		margin: 0;
	}
	.responsive-card .entry-meta div {
		border: 1px solid blue;
	}
	.responsive-card .card-media {
		background-image:
		linear-gradient(to top, var(--bright-yellow), var(--bright-yellow-transparent)),
		url('cat.png');
	}
	@media only screen and (max-width: 767px) {
		.responsive-card {
			flex-direction: column;
		}
		.responsive-card .card-media {
			min-height: 170px;
		}
		.responsive-card .entry-date {
			display: block;
			float: right;
		}
	}
</style>
