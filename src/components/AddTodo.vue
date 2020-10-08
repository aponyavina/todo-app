<template>
    <form @submit.prevent="onSubmit">
        <input type="text" v-model="title">
        <button type="submit">Create</button>
    </form>
</template>

<script>
    export default {
        name: "AddTodo",
        data() {
            return {
                title: ''
            }
        },
        methods: {
            onSubmit() {
                if (this.title.trim()) {
                    const newTodo = {
                        id: Date.now(),
                        title: this.title,
                        completed: false
                    }
                    this.$emit('add-todo', newTodo)
                    this.title = ''
                }
            }
        }
    }
</script>

<style scoped>
    form {
        display: flex;
        margin: 10px 0;
        align-items: center;
        justify-content: center;
    }

    input {
        width: 400px;
        margin-right: 20px;
    }

    button {
        background: rgba(16, 13, 250, 0.76);
        border: none;
        color: #fff;
        padding: 5px 7px;
        border-radius: 3px;
    }
</style>