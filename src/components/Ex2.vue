<script>
    export default { 
        data() {
            return {
                width: '800',
                height: '400',
                myImg: '/assets/me.png'
            }
        },
    }
</script>

<template>

    <!-- add code here -->
    <!-- v-bind: ...... same as v: ..... -->
    <img v-bind:src="myImg" alt="" v-bind:width="width" v-bind:height="height">
   
</template>
