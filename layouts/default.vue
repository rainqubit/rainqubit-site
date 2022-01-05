<template>
<main id="main-container" class="text-white bg-black min-v-screen">
    <div id="header">
        <div class="header">
            <h1 class="text-5xl">XOX</h1>
            <p>rainqubit</p>
        </div>
    </div>
    <div id="sidebar">
        <h1>sidebar</h1>
    </div>
    <div id="content" class="content">
        <Nuxt />
    </div>
</main>

</template>

<script>
export default {
    name: "Default",
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Overpass+Mono:wght@300;400;500;600;700&display=swap');

#main-container{
    font-family: 'Overpass Mono', monospace;
    display: grid;
    grid-template: 
    "header header"
    "sidebar content";
    grid-template-columns: 10rem auto;
    grid-template-rows: 5rem auto;
    padding: 0 15rem 0 15rem;
    min-height: 100vh;
}

#header{
    grid-area: header;
}

#sidebar{
    grid-area: sidebar;
}

#content{
    grid-area: content;
}

.header{
    display: flex;
    flex-direction: row;
    align-items: center;
    min-height: 100%;
    padding: 0 2rem 0 2rem;
}

.header > * {
    margin: 0 0.5rem 0 0.5rem;
}

.content {
    padding: 1rem;
}


</style>

