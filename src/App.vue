<template>
	<list-card :cardList="notebooksList"/>
</template>

<script>
import ListCard from './components/ListCard';
import{notebooksList} from './constants/3_data_notebooks'
export default {
	name: 'App',
	components: {
		ListCard,
	},
	data() {
		return {
			notebooksList,
		}
	},
}
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	margin-top: 60px;
}
</style>
