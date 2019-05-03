<template>
    <v-container>
        <v-layout
                text-xs-center
                wrap
        >
            <v-flex xs12>
                <hot-table :data="data" colHeaders="true" rowHeaders="true" width="600" height="300"></hot-table>
            </v-flex>


        </v-layout>
    </v-container>
</template>

<script>
    import { HotTable } from '@handsontable/vue';
    export default {
        data: () => ({
            data: [
                ['', 'Tesla', 'Mercedes', 'Toyota', 'Volvo'],
                ['2019', 10, 11, 12, 13],
                ['2020', 20, 11, 14, 13],
                ['2021', 30, 15, 12, 13]
            ],
        }),
        components: {
            HotTable
        }
    }
</script>

<style>
    @import '~handsontable/dist/handsontable.full.css';
</style>
