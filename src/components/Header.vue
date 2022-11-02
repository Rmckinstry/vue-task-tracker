<template>
  <header>
    <h1>{{ title }}</h1>
    <Button @toggle-add-task="$emit('toggle-add-task')" 
            :title="showAddTaskValue ? 'Close' : 'AddTask'" 
            :color="showAddTaskValue ? 'red' : 'green'" />
  </header>
</template>

<script>
import Button from "./Button.vue";
export default {
  name: "Header",
  props:{
    title: String,
    showAddTaskValue: Boolean,
  },
  components: {
    Button,
  },
  emits:['toggle-add-task']
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
