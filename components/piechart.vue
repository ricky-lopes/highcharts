<template>
    <div>
        <highchart :options="chartOptions"
        >
        </highchart>
    </div>
</template>
  
<script setup lang="ts">
    const props = defineProps({
        namepage: {
            type: String,
            required: true
        },
        datas: {
            type: Array
        }
    })

    const chartOptions = {
        chart: {
            plotBackgroundColor: null,
            plotBorderWidth: null,
            plotShadow: false,
            type: 'pie'
        },
        title: {
            text: props.namepage,
            align: 'left'
        },
        tooltip: {
            pointFormat: '{series.name}: <b>{point.percentage:.1f}%</b>'
        },
        accessibility: {
            point: {
            valueSuffix: '%'
            }
        },
        plotOptions: {
            pie: {
            allowPointSelect: true,
            cursor: 'pointer',
            dataLabels: {
                enabled: false
            },
            showInLegend: true
            }
        },
        series: [{
            name: 'Brands',
            colorByPoint: true,
            data: props.datas
        }]
    }
</script>