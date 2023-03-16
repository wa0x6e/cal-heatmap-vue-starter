<script setup lang="ts">
import { onMounted } from 'vue';
import CalHeatmap from 'cal-heatmap';
import Tooltip from 'cal-heatmap/plugins/Tooltip';
import 'cal-heatmap/cal-heatmap.css';

const cal = new CalHeatmap();

function paintCalendar() {
  cal.paint({}, [[Tooltip]]);
}

onMounted(() => paintCalendar());
</script>

<template>
  <div id="cal-heatmap"></div>
</template>
