<template>
	<div>
		<card-note v-for="element in cardList" :key="element.id" :card="element"/>
	</div>
</template>

<script>
import CardNote from './CardNote'
export default {
	name: "ListCard",
	components: {
		CardNote,
	},
	props: {
		cardList: {
			type: Array,
			default: () => [],
		},
	}
}
</script>

<style lang="css" scoped></style>