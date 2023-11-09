<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps<{
    initialCount: number
}>()

const counter = ref<number>(props.initialCount ?? 0)
</script> 
<template>
    <slot name="top"></slot>
    <button @click="counter++">{{ counter }}</button>
    <slot name="bottom"></slot>
</template>