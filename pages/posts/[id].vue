<script setup>
const route = useRoute()
const {data: post} = await useFetch(`https://jsonplaceholder.typicode.com/posts/${route.params.id}`)
</script>

<template>
    <h1 class="text-3xl font-bold text-center">{{ post.title }}</h1>
    <p class="mt-6 mx-10">{{ post.body }}</p>

    <div class="mt-10 mx-10 text-right">
        <NuxtLink to="/posts"> Volver </NuxtLink>
    </div>
    
    
</template>
