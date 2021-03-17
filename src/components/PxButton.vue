<template>
    <button 
        @click="click"
        class="bg-transparent hover:bg-green-700 font-semibold hover:text-white">
        <slot></slot>
    </button>
</template>

<script>
    export default {
        name: 'PxButton',

        methods: {
            click(){
                this.$emit('click')
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>