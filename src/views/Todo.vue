<template>
    <div>
        <ol v-for="(todo, index) in todolist" v-bind:key="index">
            <span>{{ index + 1 }} - {{ todo.task }}</span>
        </ol>
    </div>
</template>

<script>
import { TodoItem } from '@/models/TodoItem';
export default {
    data: () => ({
        todolist: [],
    }),
    methods: { },
    mounted() {
        const todo = new TodoItem('make a todo list', false);
        const todoTwo = new TodoItem('organize my github', false);
        const todoThree = new TodoItem('learn kotlin', false);
        this.todolist = [ todo, todoTwo, todoThree ];
    },
};
</script>