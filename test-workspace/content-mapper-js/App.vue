<script>
import Generic from './Generic.vue';

export default {
	components: { Generic },
	data: () => ({ item: /** @type {any} */ ('text') }),
};
</script>

<template>
	<slot :value="1" />
	<!-- @vue-generic {{ id: number }} -->
	<Generic :item="{ id: 'wrong' }" />
	<Generic :item="item" v-slot="{ value }: { value: string }">
		{{ value.toFixed() }}
	</Generic>
</template>
