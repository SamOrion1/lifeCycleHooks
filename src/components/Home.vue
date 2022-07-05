<template>
    <div>
        <h1>{{name}}</h1>
        <p id="Demo">{{name}}</p>
    </div>
</template>

<script lang="ts">

export default {

    name : '',

    data (){
        return {name: "Rasengan", display:true}
    },

    beforeCreate(){
        this.name="Chidori"
        console.log("before create", this.name)
    },
    
    created(){
        // this.name="Chidori"
        console.log("created", this.name)
    },

    beforeMount(){
        console.log("before mount", document.getElementById('Demo'))
    },

    mounted(){
        console.log("mounted", document.getElementById('Demo'))
    },

    beforeUnmount() {
        console.log('before unmount', this.name)
    },

    unmount() {
        console.log('unmount', this.name)
    },
    
}
</script>