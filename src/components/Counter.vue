<template>
    <h1>{{title || 'counter'}}</h1>
    <p>{{counter}}</p>

    <div>
        <button v-on:click="incrementar">
            Incrementar
        </button>

        <button v-on:click="Decrementar">
            Decrementar
        </button>
    </div>
</template>

<script>
export default {

    props:{
        title: String,
        start: {
            type: Number,
            default: 100
        }
    },
    data (){
        return {
            counter: 5
        }
    },
    methods: {
        getSquareValue(){
             return this.counter * this.counter;
        },

        incrementar(){
            this.counter = this.counter + 1;
        },

        Decrementar(){
            this.counter = this.counter -1 ;
        }
    },

    computed: {
        squareCounter(){
            console.log("counter llamadao")
            return this.counter * this.counter;

        },

        customTitle(){
            return this.$props.title
        }
    }
}
</script>

<style>

</style>