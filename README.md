# cal-heatmap-vue-starter

This template should help get you started implementing and using Cal-Heatmap with Vue 3

## Install

### By cloning the current repo

Clone this git repo

`git clone git@github.com:wa0x6e/cal-heatmap-vue-starter.git`

Inside the newly cloned repo, install all the dependencies

`npm install`

Start the app

`npm run dev`

You should see a very basic cal-heatmap calendar on the homepage

### Using `create-vue`

Create a new project using create-vue

`npm init vue@latest`

Follow all the on-screen vue instructions, then add `cal-heatmap` with

`npm install cal-heatmap`

Create the file `src/components/CalHeatmap.vue`, with the following content

```
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
```

In the vue you want to display the calendar, import the component

```
import CalHeatmap from './components/CalHeatmap.vue';
```

Then display it with

```
<CalHeatmap />
```

Start your app

`npm run dev`
