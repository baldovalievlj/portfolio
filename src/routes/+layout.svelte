<script>
    import "../app.css";
    import Header from "../components/Header.svelte";
    import Footer from "../components/Footer.svelte";

    let y;
    let innerHeight = 0
    let innerWidth = 0

    function goTop() {
        document.body.scrollIntoView()
    }
</script>

<div class="relative flex flex-col h-full mx-auto w-full text-sm sm:text-base min-h-screen">
    <!--    <Header y = {y}/>-->
    <slot/>
    <Footer/>
    <div class={"fixed bottom-0 w-full duration-200 flex p-10 z-[10] " + (y > 0 ? 'opacity-full pointer-events-auto' : 'pointer-events-none opacity-0')}>
        <button on:click={goTop()}
                class="ml-auto rounded-full bg-cyan-950 text-amber-500 px-6 sm:px-4 hover:bg-cyan-800 cursor-pointer">
            <i class="fa-solid fa-arrow-up grid place-items-center aspect-square"></i>
        </button>
    </div>
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth/>