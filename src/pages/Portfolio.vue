<script>
import { store } from '../store/store';
import axios from 'axios';

    export default {
        name: 'portfolio',
        data(){
            return {
                projects: [],
            }
        },
        methods: {
            getApi(){
                axios.get(store.apiUrl + 'projects')
                    .then(result => {
                        console.log(result.data);
                    })
            }
        },
        mounted(){
            this.getApi();
        }
    }
</script>

<template>
    <h1>Portfolio</h1>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ad illo culpa sequi quod non facilis cupiditate quam rerum est ex? Sunt sed ea aspernatur dicta repellendus molestias illo voluptatum excepturi!</p>
</template>

<style scoped lang="scss">

</style>

