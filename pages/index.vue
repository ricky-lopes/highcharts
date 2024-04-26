<template>
    <div class="p-8 gap-3 flex flex-col">
        <div class="w-full flex justify-between">
            <h1 class="font-bold text-xl">Ricky Lopes</h1>
            <h1 class="font-bold text-xl">Developer</h1>
        </div>
        <div class="p-8 border border-slate-300 rounded">
            <h1 class="font-bold text-lg">PieChart</h1>
            <Piechart :namepage="'PieChart'" :datas="data"/>
        </div>

        <div class="p-8 border border-slate-300 rounded">
            <h1 class="font-bold text-lg">ColumnChart</h1>
            <Realilstchart/>
        </div>


        <div class="p-8 border border-slate-300 rounded">
            <h1 class="font-bold text-lg">LineChart</h1>
            <Linechart/>
        </div>

        <div class="p-8 border border-slate-300 rounded">
            <h1 class="font-bold text-lg">AreaChart</h1>
            <Graphchart/>
        </div>
    </div>
</template>

<script setup lang="ts">
    const data = [
        {
            name: 'Chrome',
            y: 74.77,
            sliced: true,
            selected: true
        }, 
        {
            name: 'Edge',
            y: 12.82,
        },
        {
            name: 'Firefox',
            y: 4.63
        },
        {
            name: 'Safari',
            y: 2.44
        },
        {
            name: 'Internet Explorer',
            y: 2.02
        },
        {
            name: 'Other',
            y: 3.28
        }
    ]
</script>