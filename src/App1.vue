<template>
    <JqxBarGauge ref="barGaugeReference"
        :width="600" :height="600" 
        :values="values" :formatFunction="formatFunction" 
    />
</template>
 
<script>
    import JqxBarGauge from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxbargauge.vue';
 
    export default {
        components: {
            JqxBarGauge
        },
        data: function () {
            return {
                values: [10, 20, 30, 40, 50]
            }
        },
        methods: {
            formatFunction: function (value, index, color) {
                return color;
            }
        }
    }
</script>
