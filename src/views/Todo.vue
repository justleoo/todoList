<template>
    <div>
        <ol v-for="(todo, index) in todolist" v-bind:key="index">
            <span>{{ index + 1 }} - {{ todo }}</span>
        </ol>
    </div>
</template>

<script>
export default {
    data: () => ({
        todolist: [],
    }),
    methods: { },
    mounted() {
        this.todolist = [
            'learn kotlin',
            'make a todo list',
            'hello',
        ];
    },
};
</script>