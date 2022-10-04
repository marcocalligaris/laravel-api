<template>
    <div class="content">
        <HeaderItem :title="title" />
        <main class="container my-4">
            <h2 class="font-weight-bold">Elenco dei post</h2>
            <PostsItem />
        </main>
    </div>
</template>

<script>
import HeaderItem from './HeaderItem.vue';
import PostsItem from './posts/PostsItem.vue';

export default {
    name: "App",
    components: { HeaderItem, PostsItem },
    data() {
        return {
            title: "Boolpress",
        };
    },
};
</script>