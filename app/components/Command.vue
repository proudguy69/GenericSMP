<template>
    <span class="flex items-center gap-2">
        <code class="bg-slate-800 p-1 rounded-sm flex-1">/{{ command }}</code>
        <span class="flex-1"> - {{ action }}</span>
    </span>
</template>

<script setup>
defineProps(['command', 'action'])
</script>