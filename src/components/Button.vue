<template>
    <button @click="onClick()" :style="{ background: color }" class="btn">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: {
            type: String,
            default: 'Add task'
        },
        color: {
            type: String,
            default: 'steelblue'
        }
    },
    methods: {
        onClick() {
            this.$emit('btn-click')
        }
    }
}
</script>