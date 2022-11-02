<template>
  <button @click="$emit('toggle-add-task')" :style="{background: color}" class="btn">{{ title }}</button>
</template>

<script>
import { stringLiteral } from "@babel/types";

export default {
  title: "Button",

  props: {
    title: String,
    color: String,
  },
};
</script>
