<script context="module">
	export const prerender = true;
</script>

<script>
	import face from '../../static/face.jpg'
	import logo from '../../static/logo_white.png'
	import instagram from '../../static/instagram.png'
	import spotify from '../../static/spotify.png'
	import facebook from '../../static/facebook.png'
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
<section class="face">
	<img src={face} in:fly={{duration: 2000}} alt="Profile Phote">
</section>

<div class="fly" in:fly={{y: 40, duration: 2000}}>
	<section class="logo">
		<img src={logo} alt="TWZTD">
	</section>

	<section class="socials" in:fly={{y: 40, duration: 2000}}>
		<a target="_blank" href="https://instagram.com/TWZTDMUZIK"><img src={instagram} alt="Instagram"></a>
		<a target="_blank" href="https://twitter.com/TWZTDMUZIK"><img src={twitter} alt="Twitter"></a>
		<a target="_blank" href="https://soundcloud.com/TWZTDMUZIK"><img src={soundcloud} alt="SoundCloud"></a>
		<a target="_blank" href="https://open.spotify.com/artist/3rltKni0Xo8ReBTzjvubPF"><img src={spotify} alt="Spotify"></a>
		<a target="_blank" href="https://www.facebook.com/TWZTDMUZIK/"><img src={facebook} alt="Facebook"></a>
	</section>
</div>
{/if}

<div class="gigs">
	<a class="bit-widget-initializer" data-artist-name="Jeseph" data-display-local-dates="false" 
	data-display-past-dates="false" data-auto-style="false" data-text-color="#FFFFFF" 
	data-link-color="#c32828" data-background-color="rgba(0,0,0,0)" data-display-limit="15"
	data-display-start-time="false" data-link-text-color="#FFFFFF" data-display-lineup="true"
	data-display-play-my-city="true" data-separator-color="rgba(124,124,124,0.25)"></a>
</div>

<style>
	.face {
		text-align: center;
	}
	.face img {
		width: 100%;
		max-width: 1400px;
	}
	.logo {
		position: relative;
		text-align: center;
		margin-top: -15%;
	}
	.logo img {
		/* margin: 0 auto; */
		max-width: 900px;
		width: 60%;
	}
	.socials {
		margin-top: 5vw;
		text-align: center;
	}
	.socials img {
		margin: 10px;
		width: 8vw;
		max-width: 60px;
	}
	.gigs {
		
		max-width: 800px;
		margin: 80px auto;
	}
</style>