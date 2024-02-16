<template lang="html">
    <li @click="handleClicked">{{ item.text }}</li>
</template>

<script>
export default {
    props: ['item'],
    mounted() {
        console.warn('mounted', JSON.stringify(this.item))
    },
    methods:{
        handleClicked(){
            console.log(JSON.stringify(this.item))
            
        }
    }
}
</script>

<style lang="css" scoped></style>