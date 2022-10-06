<template>
    <div id="post-details-page">
        <h3 class="font-weight-bold mb-3">Dettagli del post</h3>
        <PostCardItem :post="post" />
    </div>
</template>

<script>
import Axios from 'axios';
import PostCardItem from '../posts/PostCardItem.vue';
export default {
    name: "PostPage",
    data() {
        return {
            post: null
        };
    },
    methods: {
        getPost() {
            Axios.get("http://localhost:8000/api/posts/1")
                .then(res => {
                this.post = res.data;
            }).then(() => {
                console.log("Chiamata terminata");
            });
        },
    },
    mounted() {
        this.getPost();
    },
    components: { PostCardItem }
};
</script>

<style>

</style>