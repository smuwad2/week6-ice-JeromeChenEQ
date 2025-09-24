<script>
    export default { 
        data() {
            return {
                // Add code here
                id: "blueBox",
                buttonStatus: true,
                class1: "m-2",
                class2: "",


            }
        },
        methods: { 
   			// Add code here
            changeColor() {
                if (this.buttonStatus == true) {
                    this.buttonStatus = false;
                    this.id = "redBox"
                }
                else {
                    this.buttonStatus = true;
                    this.id = "blueBox"
                }
		    }
        }
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" class="m-2" v-bind:class="{'blueBox': buttonStatus, 'redBox': !buttonStatus}">
            div ID : {{id}} 
        </div>
        
        <button type="button" v-on:click="changeColor()">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
