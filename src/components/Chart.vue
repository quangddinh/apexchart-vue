<template>
    <h1>chart {{ text }}</h1>
    <div id="chart">
        <apexchart type="line" height="550" width="950" :options="chartOptions" :series="series">a</apexchart>
    </div>
</template>

<script>
export default {
    name: 'Chart',
    data() {
        return {
            text: 'azzzz',
            series: [
                {
                    name: 'Val1',
                    data: [0, 11, 40, 40, 40, 40],
                },
                {
                    name: 'Val2',
                    data: [40, 40, 40, 40, 40, 40],
                },
                {
                    name: 'Val3',
                    data: [0, 0, 0, 12, 24, 37],
                },
                {
                    name: 'Val4',
                    data: [10, 10, 25, 40, 55, 70],
                },
                {
                    name: 'Val5',
                    data: [0, 80, 80, 80, 80, 80],
                },
                {
                    name: 'Val6',
                    data: [95, 75, 75, 75, 75, 75],
                },
                {
                    name: 'Val7',
                    data: [0, 0, 0, 0, 0, 0],
                },
                {
                    name: 'Val80',
                    data: [0, 0, 0, 0, 0, 0],
                },
            ],
            chartOptions: {
                chart: {
                    type: 'line',
                    zoom: {
                        enabled: false,
                    },
                },
                dataLabels: {
                    enabled: false,
                    // formatter: function(val, opt) {
                    //     return opt.w.globals.labels[opt.dataPointIndex];
                    // },
                },
                colors: ['#ff3838', '#3ae374', '#273c75', '#ff9f1a', '#fff200', '#0abde3', '#f78fb3', '#d1ccc0'],
                stroke: {
                    curve: 'straight',
                },
                title: {
                    text: 'Product Trends by Month',
                    align: 'center',
                },
                grid: {
                    column: {
                        colors: ['#0D3182'], // takes an array which will be repeated on columns
                    },
                    yaxis: {
                        lines: {
                            show: false,
                        },
                    },
                },
                xaxis: {
                    categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep'],
                    title: {
                        text: 'Month',
                    },
                },
                yaxis: {
                    title: {
                        text: 'Percentage',
                    },
                    min: 0,
                    max: 100,
                },
                legend: {
                    show: true,
                    fontSize: '16px',
                    //align: 'center',
                    horizontalAlign: 'right',
                    position: 'right',
                    floating: false,
                    offsetX: 1,
                    offsetY: 18,
                    // order legend
                    inverseOrder: false,
                    markers: {
                        width: 100,
                        height: 29,
                        strokeWidth: 5,
                        //strokeColor: '#FFFF',
                        fillColors: [
                            '#ff3838',
                            '#3ae374',
                            '#273c75',
                            '#ff9f1a',
                            '#fff200',
                            '#0abde3',
                            '#f78fb3',
                            '#d1ccc0',
                        ],
                        radius: 2,
                        // customHTML: function() {
                        //     return '<p>hello</p>';
                        // },
                        offsetX: 0,
                        offsetY: 3,
                    },
                    itemMargin: {
                        //  horizontal: 5,
                        vertical: 10,
                    },
                },
                markers: {
                    size: 0.5,
                },
            },
        };
    },
};
</script>

<style scoped></style>
