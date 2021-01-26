<template>
    <div>
        <h3>我是子组件</h3>
        <p>{{title}}</p>
        <button @click="modify">点击我修改</button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                temp: true,
                name: ''
            }
        },
        methods: {
            modify() {
                this.temp = !this.temp
                this.name = this.temp? '比尔·盖茨' : '乔布斯'
                this.$emit('update:title', this.name)
            }
        },
        props: ['title']
    }
</script>

<style scoped>

</style>
