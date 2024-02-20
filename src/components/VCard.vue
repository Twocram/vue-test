<script setup lang="ts">
withDefaults(defineProps<{
    text: string,
}>(), {
    text: "Some Card Text"
})
</script>

<template>
    <div class="card-container">
        {{ text }}
    </div>
</template>

<style scoped>
.card-container {
    width: 300px;
    height: 200px;
    background-color: #e0e0e0;
    border-radius: 10px;
    padding: 10px;
    font-size: 18px;
    margin-bottom: 10px;
}

.card-container:last-child {
    margin-bottom: 0;
}
</style>