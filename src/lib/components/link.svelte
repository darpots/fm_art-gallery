<script>
	export let direction = 'right';
	export let url = '/';
</script>

<div>
	<a class="link-container" href={url}>
		{#if direction === 'left'}
			<div class="link-arrow">
				<img src="/images/icon-arrow-left.svg" alt="left arrow" />
			</div>
		{/if}
		<p class="link-text">
			<slot />
		</p>

		{#if direction === 'right'}
			<div class="link-arrow">
				<img src="/images/icon-arrow-right.svg" alt="right arrow" />
			</div>
		{/if}
	</a>
</div>

<style lang="scss">
	div {
		display: inline-block;
	}

	.link-container {
		display: flex;
		text-decoration: none;
		
		.link-arrow {
			background: var(--primary);
			padding: 24px;
			transition: all .4s ease-in-out;
		}
		
		img {
			width: 8px;
		}
		
		.link-text {
			font-family: var(--headingFont);
			background-color: var(--black);
			text-transform: uppercase;
			font-style: normal;
			font-weight: 800;
			font-size: 20px;
			line-height: 24px;
			letter-spacing: 3.63636px;
			padding: 24px 35px 24px 32px;
			color: var(--white);
			transition: all .4s ease-in-out;
		}
		&:hover {
			
			.link-arrow {
				background: var(--black);
			}
			.link-text {
				background: var(--primary);
			}
		}
	}
</style>
