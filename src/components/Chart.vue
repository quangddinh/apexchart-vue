<template>
    <div id="chart">
        <apexchart type="line" height="550" width="950" :options="chartOptions" :series="series"></apexchart>
    </div>
</template>

<script>
const myColor = ['#ff3838', '#3ae374', '#273c75', '#ff9f1a', '#fff200', '#0abde3', '#f78fb3', '#d1ccc0'];
export default {
    name: 'Chart',
    data() {
        return {
            series: [
                {
                    name: '',
                    data: [0, 11, 40, 40, 40, 40],
                },
                {
                    name: '',
                    data: [40, 40, 40, 40, 40, 40],
                },
                {
                    name: '',
                    data: [0, 0, 0, 12, 24, 37],
                },
                {
                    name: '',
                    data: [10, 10, 25, 40, 55, 70],
                },
                {
                    name: '',
                    data: [0, 80, 80, 80, 80, 80],
                },
                {
                    name: '',
                    data: [95, 75, 75, 75, 75, 75],
                },
                {
                    name: '',
                    data: [0, 0, 0, 0, 0, 0],
                },
                {
                    name: '',
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
                // dataLabels: {
                //     enabled: false,
                // },
                colors: myColor,
                stroke: {
                    curve: 'straight',
                },
                title: {
                    text: '',
                    align: 'center',
                },
                grid: {
                    row: {
                        colors: ['#00000'],
                    },
                    column: {
                        colors: ['#00000'],
                    },
                    yaxis: {
                        lines: {
                            show: false,
                        },
                    },
                },
                xaxis: {
                    title: {
                        text: '',
                    },
                },
                yaxis: {
                    color: '#63C7A4',
                    show: true,
                    title: {
                        text: '',
                    },
                    min: 0,
                    max: 100,
                },
                legend: {
                    show: true,
                    fontSize: '16px',
                    horizontalAlign: 'right',
                    position: 'right',
                    offsetX: 1,
                    offsetY: 18,
                    inverseOrder: false,
                    markers: {
                        width: 100,
                        height: 29,
                        strokeWidth: 5,
                        fillColors: myColor,
                        radius: 2,
                        offsetX: 0,
                        offsetY: 3,
                    },
                    itemMargin: {
                        vertical: 10,
                    },
                },
                markers: {
                    size: 0.5,
                },
            },
        };
    },
    mounted() {
        this.$forceUpdate();
    },
};
</script>

<style scoped></style>
