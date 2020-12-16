<script>
    import Home from "./pages/Home.svelte";
    import NotFound from "./pages/NotFound.svelte";
    import Community from "./pages/Community.svelte";
    import Router from "svelte-spa-router";
    import Navbar from "./components/Navbar.svelte";
    import Footer from "./components/Footer.svelte";

    const routes = {
        "/": Home,
        "/community": Community,
        "*": NotFound,
    };
</script>

<style global lang="postcss">
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
</style>

<main>
    <Navbar />
    <Router {routes}/>
    <Footer/>
</main>
