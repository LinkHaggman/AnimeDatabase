<template>
	<div class="card">
		<a :href="anime.url" target="_blank">
			<img 
				:src="anime.image_url" 
				:alt="anime.title + ' Poster'" 
			/>
			<h3>{{ anime.title }}</h3>
		</a>
	</div>
</template>

<script>
export default {
	props: ['anime']
}
</script>

<style lang="scss" scoped>
.card {

	width: 20%;
	padding: 0px 8px;
	margin-bottom: 16px;

	img {
		width: 70%;
		height: 70%;
		object-fit: cover;
		border-radius: 16px;
		box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.15);
		transition: 0.4s;
	}

	h3 {
		padding: auto;
		color: #dfdfdf;
		transition: .4s;
	}

	&:hover {
		img {
			transform: scale(1.05);
		}

		h3 {
			color: #4c8fe6;
		}
	}
}

@media (max-width: 768px) {
	.card {
			width: 25%;
}
  .card h3 {
			font-size: 90%;
}
}
@media (max-width: 425px) {
   .card {
			width: 50%;
}
  .card h3 {
			font-size: 80%;
}
}
@media (max-width: 320px) {
  .card h3 {
			font-size: 60%;
}
}
</style>