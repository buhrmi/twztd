<script context="module">
	export const prerender = true;
</script>

<script>
	import face from '../../static/face.jpg'
	import logo from '../../static/logo_white.png'
	import instagram from '../../static/instagram.png'
	import spotify from '../../static/spotify.png'
	import soundcloud from '../../static/soundcloud.png'
	import twitter from '../../static/twitter.png'
	import { fly } from 'svelte/transition'
	import { onMount } from 'svelte'
	
	let fadeIn = false

	onMount(function() {
		fadeIn = true
	})
</script>

<svelte:head>
	<title>TWZTD</title>
</svelte:head>

{#if fadeIn}
<section>
	<img src={face} in:fly={{duration: 2000}} alt="Profile Phote" class="face">
</section>

<div class="fly" in:fly={{y: 40, duration: 2000}}>
	<section class="logo">
		<img src={logo} alt="TWZTD" >
	</section>

	<section class="socials" in:fly={{y: 40, duration: 2000}}>
		<a target="_blank" href="https://instagram.com/TWZTDMUZIK"><img src={instagram} alt="Instagram"></a>
		<a target="_blank" href="https://twitter.com/TWZTDMUZIK"><img src={twitter} alt="Twitter"></a>
		<a target="_blank" href="https://soundcloud.com/TWZTDMUZIK"><img src={soundcloud} alt="SoundCloud"></a>
		<a target="_blank" href="https://open.spotify.com/artist/3rltKni0Xo8ReBTzjvubPF"><img src={spotify} alt="Spotify"></a>
	</section>
</div>
{/if}


<style>
	.face {
		width: 100%;
	}
	.logo {
		position: relative;
		text-align: center;
		margin-top: -15%;
	}
	.logo img {
		/* margin: 0 auto; */
		width: 60%;
	}
	.socials {
		margin-top: 5vw;
		text-align: center;
	}
	.socials a {
		margin: 10px;
	}
	.socials img {
		max-width: 10vw;
	}
</style>