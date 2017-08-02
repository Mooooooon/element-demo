<template>
    <div class="chart">
        <canvas id="myChart"></canvas>
    </div>
</template>

<script>
  import Chart from 'chart.js'

  export default {
    name: 'chart',
    data () {
      return {
        myChart: null
      }
    },
    props: ['chartData'],
    mounted () {
      let ctx = document.getElementById('myChart').getContext('2d')
      this.myChart = new Chart(ctx, {
        type: 'line',
        data: {
          labels: new Array(10),
          datasets: [{
            label: 'label',
            data: this.chartData,
            lineTension: 0,
            fill: false,
            pointRadius: 0,
            borderWidth: 1,
            borderColor: '#36a2eb'
          }]
        }
      })
    }
  }
</script>
