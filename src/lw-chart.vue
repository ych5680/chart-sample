<script setup>
    import { onMounted, ref } from 'vue';
    import { createChart } from 'lightweight-charts';

    let chart;
    const chartContainer = ref();

    onMounted(() => {
        // Create the Lightweight Charts Instance using the container ref.
        chart = createChart(chartContainer.value);
    });

    
</script>
<template>
    <div class="lw-chart" ref="chartContainer"></div>
</template>
<style scoped>
    .lw-chart {
        height: 100%;
    }
</style>