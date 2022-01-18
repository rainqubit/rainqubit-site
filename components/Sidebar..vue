<template>
<div>
    <div v-for="link in links" :key="link.label">
        <NuxtLink :to="link.link">{{link.label}}</NuxtLink>
    </div>
</div>
</template>
<script>
export default{
    computed: {
        links() {
            return this.$store.state.navs.links
        }
    },
    mounted() {
        console.log(this.$store.state.navs.links)
    }
}
</script>