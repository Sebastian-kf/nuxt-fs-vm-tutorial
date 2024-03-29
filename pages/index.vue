<script setup>
	const { data: ditto, error } = await useFetch('/api/ditto')
</script>
<template>
	<h1>Hello World</h1>
	<ul v-if="ditto">
		<li>
			<img :src="ditto.sprite" />
		</li>
		<li>
			{{ ditto.id }}: {{ ditto.name }}
		</li>
	</ul>
	<div v-else>
		<p>{{ error }}</p>
	</div>
</template>