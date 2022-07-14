<script lang="ts">
	import Upgrades from '../lib/Upgrades.svelte'

	let cuddleCount = 0
</script>

<div id="fluffy-cuddles__app-wrapper">
	<Upgrades />
	<div>
		<span>
			You have cuddled this cutie {cuddleCount} times
		</span>
		<img src="" alt="asdasd" />
	</div>
	<footer class="absolute bottom-0 p-4">
		&copy; {new Date().getFullYear()} skepfusky
	</footer>
</div>
