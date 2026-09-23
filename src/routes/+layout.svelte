<script>
	import favicon from '$lib/assets/favicon.svg';
  import '../app.css'
  import Header from '../components/Header.svelte'
  import Footer from '../components/Footer.svelte'

	let { children } = $props();

  let y = $state(0);
  let innerHeight = $state(0);
  let innerWidth = $state(0);

  function goUp() {
      document.body.scrollIntoView()
    }
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen">
  <!-- <div class={"fixed bottom-0 w-full duration-200 flex p-10 z-[10] " + y > 0 ? 'opacity-full pointer-events-auto' : 'pointer-events-none opacity-0'}>
    <button on:click={goUp} class="ml-auto rounded-full aspect-square bg-slate-900 text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer">
      <i class="fa-solid fa-arrow-up place-items-center aspect-square"></i>
    </button>
  </div> -->

  <Header y={y}/>
  {@render children()}
  <Footer/>
</div>


<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />

