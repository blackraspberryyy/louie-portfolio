<template>
	<div>
		<VApp class="app">
			<VMain>
				<slot />
			</VMain>
		</VApp>
	</div>
</template>

<style scoped>
	.app {
		background-color: #e5e5f7;
		background-image:  repeating-radial-gradient( circle at 0 0, transparent 0, #e5e5f7 40px ), repeating-linear-gradient( #ddf0ff55, #ddf0ff );
	}
</style>