<script lang="ts">
	import Upgrades from "../lib/Upgrades.svelte"

	let cuddleCount = 0

	function pat() {
		cuddleCount += 1
	}
</script>

<div id="fluffy-cuddles__app-wrapper">
	<div class="cutie-container">
		<span> You have cuddled this cutie </span>
		<span>{cuddleCount}</span>
		<img
			class="cutie"
			src="https://github.com/skepfusky.png"
			alt="Pat me uwu"
			on:click={pat}
		/>
	</div>
	<Upgrades />
	<footer>
		&copy; {new Date().getFullYear()} skepfusky
	</footer>
</div>

<style lang="scss">
	#fluffy-cuddles__app-wrapper {
		display: grid;
		gap: 1rem;
		grid-template-columns: repeat(3, 1fr);
		grid-template-rows: repeat(2, 1fr);
		grid-template-areas:
			"cutie cutie upgrades"
			"footer footer footer";
	}

	.cutie-container {
		grid-area: cutie;
		display: flex;
		flex-direction: column;
		align-items: center;
		row-gap: 0.99rem;
		border-radius: 7px;
		padding: 0.5rem;
		box-shadow: 0 12px 16px rgba(black, 25%);
	}

	.cutie {
		--scale: 1;
		border-radius: 50%;
		width: 250px;
		transform: scale(var(--scale));
		transition: transform 150ms cubic-bezier(0, 0.83, 0.25, 1);
		cursor: pointer;
		-moz-user-drag: none;
		-webkit-user-drag: none;
		user-select: none;

		&:hover {
			--scale: 1.055;
		}
		&:active {
			--scale: 1.015;
		}
	}

	footer {
		grid-area: footer;
		box-shadow: 0 0 16px rgba(black, 25%);
		padding: 0.5rem;
		height: min-content;
	}
</style>
