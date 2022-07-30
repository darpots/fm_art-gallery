<script>
	import Link from '../components/link.svelte';
</script>

<section class="hero-section">
	<div class="hero-image">
		<picture>
			<source
				srcset="/images/desktop/image-hero@2x.jpg 2x, /images/desktop/image-hero.jpg"
				media="(min-width: 1440px)"
			/>
			<source
				srcset="/images/tablet/image-hero@2x.jpg 2x, /images/tablet/image-hero.jpg"
				media="(min-width: 768px)"
			/>
			<img
				srcset="/images/mobile/image-hero@2x.jpg 2x"
				src="/images/mobile/image-hero.jpg"
				alt="hero"
			/>
		</picture>
	</div>

	<div class="grid">
		<h1>MODERN <br /> ART GALLERY</h1>
		<p>
			The arts in the collection of the Modern Art Gallery all started from a spark of inspiration.
			Will these pieces inspire you? Visit us and find out.
		</p>
		<div class="link">
			<Link url="/location">our location</Link>
		</div>
	</div>
</section>

<style lang="scss">
	.hero-section {
		position: relative;
		width: 375px;
		margin-inline: auto;

		@media screen and (min-width: 768px) {
			width: 768px;
		}

		@media screen and (min-width: 1440px) {
			width: 1440px;
		}
	}

	.hero-image {
		width: 375px;

		@media screen and (min-width: 768px) {
			width: 437px;
		}
		@media screen and (min-width: 1440px) {
			width: 540px;
			position: relative;
			left: 431px;

			&:before {
				content: '';
				position: absolute;
				inset: 0;
				left: -438px;
				z-index: -10;
				background-color: var(--black);
				height: 800px;
			}
		}
	}

	h1 {
		font-weight: 900;
		font-size: 60px;
		line-height: 55px;
		color: var(--black);

		@media screen and (min-width: 768px) {
			font-size: 70px;
			line-height: 65px;
		}

		@media screen and (min-width: 1440px) {
			font-size: 96px;
			line-height: 88px;
			width: 514px;
			position: relative;
			background: linear-gradient(to right,  var(--white) 287px, var(--black) 1%,);
			background-repeat: no-repeat;
			background-size: cover;
			background-clip: text;
			-webkit-background-clip: text;
			color: transparent;
		}
	}

	p {
		font-weight: 300;
		font-size: 18px;
		line-height: 28px;
		color: var(--gray);

		@media screen and (min-width: 1440px) {
			width: 350px;
			font-size: 22px;
			line-height: 32px;
		}
	}
	.grid {
		display: grid;
		gap: 32px;
		margin-left: 16px;
		margin-right: 16px;
		margin-top: 32px;

		@media screen and (min-width: 768px) {
			margin: 0;
			width: 339px;
			gap: 48px;
			position: absolute;
			top: 145px;
			right: 40px;
		}

		@media screen and (min-width: 1440px) {
			width: 1110px;
			top: 189px;
			left: 0;
			margin-inline: auto;
			gap: 64px;
			column-gap: 246px;
			grid-template-columns: 1fr 1fr;

			.link {
				grid-column: 2;
			}
		}
	}
</style>
