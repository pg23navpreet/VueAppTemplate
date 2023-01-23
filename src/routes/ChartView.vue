<!--
VFS VUE Single File Component
Copyright (c) 2018. Scott Henshaw, Kibble Online Inc. All Rights Reserved.
-->
<script>
    import Controller from '@/plugins/controller'

    class ChartController extends Controller {

        constructor( name, subComponentList = []) {
            super( name, subComponentList );
            this.vm = {
                name: 'Chart Page',
            }
        }
    }

    export default new ChartController('Chart');

</script>
<template>

    <section class="flexbox columns chart">
        
    </section>

</template>
<style scoped>
/* Local styles for this template */
    .chart {
        /* display: block; */
        margin:2vw;
        border: 1px solid black;
        background-color: lightgray;
        color: black;
        height: 78vh;
        width: 80vw;
    }

</style>

