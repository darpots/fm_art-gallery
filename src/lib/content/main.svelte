<main>
	<div class="flex">
		<div class="flip-order">
			<h2>Your Day at the Gallery</h2>
			<p>
				Wander through our distinct collections and find new insights about our artists. Dive into
				the details of their creative process.
			</p>
		</div>
		<div>
			<picture>
				<source
					srcset="/images/desktop/image-grid-1@2x.jpg 2x, /images/desktop/image-grid-1.jpg"
					media="(min-width: 1440px)"
				/>
				<source
					srcset="/images/tablet/image-grid-1@2x.jpg 2x, /images/tablet/image-grid-1.jpg"
					media="(min-width: 768px)"
				/>
				<img
					srcset="/images/mobile/image-grid-1@2x.jpg 2x"
					src="/images/mobile/image-grid-1.jpg"
					alt="hero"
				/>
			</picture>
		</div>
	</div>

	<div class="flex">
		<div>
			<picture>
				<source
					srcset="/images/desktop/image-grid-2@2x.jpg 2x, /images/desktop/image-grid-2.jpg"
					media="(min-width: 1440px)"
				/>
				<source
					srcset="/images/tablet/image-grid-2@2x.jpg 2x, /images/tablet/image-grid-2.jpg"
					media="(min-width: 768px)"
				/>
				<img
					srcset="/images/mobile/image-grid-2@2x.jpg 2x"
					src="/images/mobile/image-grid-2.jpg"
					alt="hero"
				/>
			</picture>
		</div>
		<div>
			<div>
				<picture>
					<source
						srcset="/images/desktop/image-grid-3@2x.jpg 2x, /images/desktop/image-grid-3.jpg"
						media="(min-width: 1440px)"
					/>
					<source
						srcset="/images/tablet/image-grid-3@2x.jpg 2x, /images/tablet/image-grid-3.jpg"
						media="(min-width: 768px)"
					/>
					<img
						srcset="/images/mobile/image-grid-3@2x.jpg 2x"
						src="/images/mobile/image-grid-3.jpg"
						alt="hero"
					/>
				</picture>
			</div>
			<div>
				<h2>COME & BE INSPIRED</h2>
				<p>
					We’re excited to welcome you to our gallery and see how our collections influence you.
				</p>
			</div>
		</div>
	</div>
</main>



<style lang="scss">
  main {
    width: 343px;
    margin-inline: auto;

    @media screen and (min-width: 768px){
      width: 689px;
    }

    @media screen and (min-width: 1440px){
      width: 1110px;
    }
  }
  .flex {
    display: flex;
    flex-direction: column;
    gap: 30px;

    @media screen and (min-width: 768px){
      flex-direction: row;
    }
  }

  .flip-order {
    order: 1;

    @media screen and (min-width: 768px) {
      order: initial;
    }
  }
</style>

