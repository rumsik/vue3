<template>
    <form @submit.prevent>
        <h4>Создание поста</h4>
        <input 
        v-model="post.title"
        class="input"
        type="text"
        placeholder="Название"
        >
        <input
        v-model="post.body"
        class="input"
        type="text"
        placeholder="Описание"
        >
        <button
        class="btn"
        @click="createPost"
        >
        Создать
        </button>
        

    </form>

</template>

<script>
export default {
    data() {
        return {
            post: {
                body: '',
                title: '',
            },
            
        }
        
    },
    methods: {
        createPost() {
            this.post.id = Date.now();
            this.$emit('create', this.post, 'second parametr', '3 parametr');
            this.post = {
                title: '',
                body: '',
            }
        },
    }
 
}


</script>



<style>
.input {
    width: 100%;
    border: 1px solid teal;
    padding: 10px 15px;
    margin-top: 15px;
}
.btn {
    margin-top: 15px;
    align-self: flex-end;
    padding: 10px 15px;
    background: none;
    color: teal;
    border: 1px solid teal;
}
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}


</style>