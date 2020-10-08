<template>
    <div>
        <ul>
            <TodoItem
            v-for="(todo, i) of todos"
            v-bind:todo="todo"
            v-bind:index="i"
            v-on:remove-todo="removeTodo"
            />
        </ul>
    </div>
</template>

<script>
    import TodoItem from '@/components/TodoItem'
    export default {
        props: ['todos'],
        components: {
            TodoItem
        },
        methods: {
            removeTodo(id) {
                this.$emit('remove-todo', id)
            }
        }
    }
</script>

<style scoped>
    ul {
        list-style: none;
        margin: 20px auto 0 auto;
        padding: 0;
        max-width: 500px;
    }
</style>