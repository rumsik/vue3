<template>
    <div>
        <div class="post" v-for="post in posts"
        :key="post.id">
            <div><strong>Название </strong>{{ post.title }}</div>
            <div><strong>Описание</strong> {{ post.body }}</div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true,
        }
    }
}
</script>



<style>
.post {
    padding: 15px;
    border: 2px solid teal;
    margin-top: 15px;
}
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

</style>