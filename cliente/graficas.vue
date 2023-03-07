<template>
	<Bar
	  id="my-chart-id"
	  :options="chartOptions"
	  :data="chartData"
	/>
  </template>
  
  <script>
  import { Bar } from 'vue-chartjs'
  import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'
  
  ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)
  
  export default {
	name: 'BarChart',
	components: { Bar },
	data() {
	  return {
		chartData: {
		  labels: [ 'Cire', 'Soku', 'BaiSupreme','Crash_bones03' ],
		  datasets:  { data: [400, 200, 120] } 
		},
		chartOptions: {
		  responsive: true
		}
	  }
	}
  }
  </script>