<template>
	<div class="container">
		<div class="image">
			<img :src="card.imgSrc">
		</div>
		<div class="content">
			<a :href="card.link">
				{{ card.title }}
			</a>
			<h5>
				Ваша економія : <span class="color">{{ card.discount }} ₴</span>
			</h5>
			<div class="price">
				<div>
					<h3>
						<span class="span">{{ card.oldPrice }}</span> ₴
					</h3>
					<h2 class="color">
						{{ card.price }} ₴
					</h2>
				</div>
				<button>Купити</button>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "CardNote",
	props: {
		card: {
			type: Object,
			default: () => ({}),
		}
	}
}
</script>

<style lang="css" scoped>
.container {
	display: flex;
	justify-content: center;
}
.content {
	padding: 10px;
	width: 450px;
}
button {
	height: 20px;
	margin-bottom: 16px;
	background-color: green;
}

.image {
	width: 200px;
}

img {
	width: 200px;
}
.span {
	text-decoration: line-through;
}
.color {
	color: red
}

.price {
	display: flex;
	justify-content: space-between;
	align-items: end;
}
</style>