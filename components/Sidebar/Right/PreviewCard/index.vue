<template>
    <div class="m-2 border bg-gray-50" 
    :class="twitterBorderColor">
       <h1>
        {{ props.title}}
        </h1>
    </div>
</template>


<script setup>
    const {twitterBorderColor} = useTailwindConfig()
    const props = defineProps({
        title: {
            type: String,
            required: true
        }
    })
</script>