<script setup lang="ts">
defineProps<{
    outline?: boolean,
    // some other props
}>()
</script>

<template>
    <button class="button" :class="{ outline }">
        <slot></slot>
    </button>
</template>

<style scoped>
.button {
    width: 352px;
    height: 52px;
    background-color: #ffffff;
    font-weight: 500;
    outline: none;
    border: none;
    font-size: 16px;
    border-radius: 12px;
    cursor: pointer;
    color: #017CFE;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 10px;
}

.button.outline {
    background-color: #2D93FF;
    color: #ffffff;
}
</style>