// SFC Single File Componet
<template>
    <h1 class="text-danger">Text : {{ x }}</h1>
</template>

<script setup>
    import { ref } from 'vue';
    const x = ref('Hè lô');
</script>

<style scoped></style>