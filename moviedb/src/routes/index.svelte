<script context="module">
	// @ts-ignore
	export async function load({ fetch }) {
		const res = await fetch(
			`https://api.themoviedb.org/3/movie/popular?api_key=75018238f7641d4a966cb8d2ca0702a9&language=pt-BR&page=1`
		);

		const data = await res.json();
		console.log(data);
		if (res.ok) {
			return {
				props: { popular: data.results }
			};
		}
	}
</script>

<script>
	// @ts-nocheck

	import PopularMovies from '../components/PopularMovies.svelte';
	import SearchMovies from '../components/SearchMovies.svelte';
	export let popular;
	import { fly } from 'svelte/transition';
</script>

<section in:fly={{y: 50, duration: 500, delay: 500}} out:fly={{y:50, duration: 500}}>
	<SearchMovies />
	<PopularMovies {popular} />
</section>
