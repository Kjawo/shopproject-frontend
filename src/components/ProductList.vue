<template>
    <div>
        <h1>Products:</h1>
        <p>{{JSON.stringify(info)}}</p>
    </div>
</template>

<script>

    import axios from 'axios';

    // import constants from '../constants'

    export default {
        name: "ProductList",
        data() {
            return {
                info: ''
            }
        },
        mounted () {
            axios
                .get('http://localhost:3000/shop/products')
                .then(response => (this.info = response))
        }
    }


</script>

<style scoped>

</style>