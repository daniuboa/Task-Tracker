<template>
  <div v-for="task in tasks" :key="task.id">
    <Task @delete-task="$emit('delete-task', task.id)" :task="task" />
  </div>
</template>

<script>
import Task from './Task.vue'
export default {
    name: 'Tasks',

    components: {
        Task
    },

    emits: ['delete-task'],

    props: {
        tasks: Array
    }
}
</script>

<style>

</style>