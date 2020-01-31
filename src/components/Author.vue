<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="~/assets/images/lkmx_logo.svg" width="190" height="64" blur="0" />

		<h1 v-if="showTitle" class="author__site-title" on-click="ga('send', 'event', 'home', 'titulo página', 'click en título')">
			{{ $static.metadata.siteName }}
		</h1>
<section class="author__intro">
	<h2>Lee antes de iniciar</h2>
	<p>
			A continuación encontrarás una serie de misiones que nos permitirán evaluar el desempeño de nuestro sistema, siéntete libre de explorar el sitio, pero asegurate de llevar a cabo las misiones, al terminar cada una de ellas regresa a este sitio para encontrar instrucciones sobre tu siguiente misión.
		</p>
</section>
		

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: var(--content-width);
	text-align: center;
	padding: calc(var(--space) / 2) 0 0 0;

	&__image {
		width: 190px;
		height: 64px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: 1;
		background: #FF2D55;
		padding: 2rem;
		margin-bottom: var(--space);
		color: white;
		h2 {
			margin: 0 0 1rem 0;
			color: white;
		}
	}

	&__site-title {
		font-size: 1.5em;
		margin: 0 0 var(--space) 0;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
