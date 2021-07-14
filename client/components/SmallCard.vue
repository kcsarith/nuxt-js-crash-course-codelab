<template>
    <NuxtLink class="card-container" :to="`products/${card.id}`">
        <img :src="require(`../static/images/${card.image}` || fel.jpg)" alt="" class="image">
    </NuxtLink>
</template>

<script>
    export default {
        props:["card"]
    }
</script>

<style scoped>
    .card-container {
        width: 24%;
        height: 12.5rem;
        border-radius: 0.5rem;
        overflow: hidden;
        margin-bottom: 1.5rem;
        cursor: pointer;
    }
    .image {
        width: 100%;
        height: 100%
    }
</style>
