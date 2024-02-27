<template>
    <div>
    <h1 style="margin-block-end: 5px;">{{ counter }}</h1>
    <button @click="incremento" style="margin-bottom:10px;"> + </button>
    <button @click="reset" style="margin-top:10px;"> - </button>

    </div>
    <div>
    <img :src="require('../assets/img/fondo.jpg')" alt="fondo" style="width: 500px; height: auto;">
    </div>
</template>

<script>

    import { ref } from'vue';

    export default{
    setup() {
        const counter= ref(0);
        return{counter};
    },

    methods: {
        incremento(){
            this.counter++;
        },

        reset(){
            this.counter = 0;
        }
    }
    }
</script>

<style>

.content-center {
    display: flex;
    flex-direction: column;
    align-items: center; 
    justify-content: center;
    height: 220px;
    text-align: center;
}
</style>