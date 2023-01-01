<template>
    <div class="app">
        <PostFrom
        @create="createPost"
        >
        </PostFrom>
        <PostList 
        v-bind:posts="posts"
        >
        </PostList>
    </div>   
</template>

<script>

import PostFrom from "./components/PostForm.vue";
import PostList from "./components/PostList.vue";


export default {
    components: {
        PostFrom, PostList
    },
    data() {
        return {
            posts: [
                {id: 1, title: 'jS 1', body: 'Описание поста 1'},
                {id: 2, title: 'jS 2', body: 'Описание поста 2'},
                {id: 3, title: 'jS 3', body: 'Описание поста 3'},
                {id: 4, title: 'jS 4', body: 'Описание поста 4'},
            ],

        }
    },
    methods: {
        createPost(post, second, third) {
            console.log(post);
            console.log(second);
            console.log(third);
        }

    }
}
</script>

<style >
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}



.app {
    padding: 20px;
}

</style>
