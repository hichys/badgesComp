<template>
    <div v-bind:class='
    [color,
    "w-fit border-solid rounded-xl px-2.5 py-1 text-xs font-semibold"
    ]'
     > {{ props.status }}  </div>
</template>

<script setup>
import { computed  } from 'vue';

const StatusToColor = {
    "Active" : "green",
    "UnPaid" : "orange",
    "Error" : "red",
    "InActive" : "red",
    
}

const colorToStyle = {
    "green" : "text-green-700 bg-green-300",
    "yellow" : "text-yellow-700 bg-yellow-300 ",
    "red" : "text-red-700 bg-red-300",
    "orange" : "text-amber-700 bg-amber-300",
}

const color = computed(() => {
    return colorToStyle[StatusToColor[props.status]]
})

const props =  defineProps({
    status: String,
})

</script>