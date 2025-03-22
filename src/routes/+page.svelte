<script>
	import { onMount } from 'svelte';
	import Chart from 'chart.js/auto';

	let chart;

	onMount(() => {
		const ctx = document.getElementById('pieChart').getContext('2d');
		chart = new Chart(ctx, {
			type: 'pie',
			data: {
				labels: ['Stocks', 'Crypto', 'Cash'],
				datasets: [{
					label: 'Portfolio Allocation',
					data: [50, 30, 20],
					backgroundColor: ['#36A2EB', '#FF6384', '#FFCE56']
				}]
			},
			options: {
				responsive: true,
				plugins: {
					legend: {
						position: 'bottom'
					}
				}
			}
		});
	});
</script>

<style>
	/* existing style logic here */
	canvas {
		max-width: 400px;
		margin: 2rem auto;
		display: block;
	}
</style>

<main>
    
<h1>Welcome to Portalyze</h1>
<h2>Next Level Portfolio Analysis</h2>
<p>Visit <a href="https://github.com/vctrjrvs/portalyze-frontend">The Portalyze Github Page</a> 
    to read the documentation
</p>

<canvas id="pieChart"></canvas>

</main>

