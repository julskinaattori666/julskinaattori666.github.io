# julskinaattori666.github.io
<!DOCTYPE html>
<html>
<head>
	<title>Countdown made by HP</title>
	<style>
		body {
			background-image: url("beach.jpg");
			background-size: cover;
			background-position: center;
			font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
			font-size: 36px;
			color: #ffffff;
			text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
		}

		h1 {
			font-size: 72px;
			text-align: center;
			margin-top: 100px;
			margin-bottom: 20px;
			text-shadow: 2px 2px 3px rgba(0, 0, 0, 0.5);
		}

		#countdown-container {
			width: 600px;
			height: 200px;
			margin: 0 auto;
			background-color: rgba(255, 255, 255, 0.7);
			border-radius: 20px;
			padding: 20px;
			box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
		}

		#countdown {
			font-size: 72px;
			text-align: center;
			margin-top: 40px;
			text-shadow: 2px 2px 3px rgba(0, 0, 0, 0.5);
			color: #333;
		}
	</style>
</head>
<body>
	<h1>TJ Costalle :D</h1>
	<div id="countdown-container">
		<p id="countdown"></p>
	</div>

	<script>
		// Set the date to count down to
		var countDownDate = new Date("Aug 10, 2023 00:00:00").getTime();

		// Update the countdown every 1 second
		var countdownInterval = setInterval(function() {
			// Get today's date and time
			var now = new Date().getTime();

			// Calculate the time remaining
			var timeRemaining = countDownDate - now;

			// Calculate days, hours, minutes, and seconds remaining
			var days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));
			var hours = Math.floor((timeRemaining % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
			var minutes = Math.floor((timeRemaining % (1000 * 60 * 60)) / (1000 * 60));
			var seconds = Math.floor((timeRemaining % (1000 * 60)) / 1000);

			// Update the HTML with the time remaining
			document.getElementById("countdown").innerHTML = days + "d " + hours + "h "
				+ minutes + "m " + seconds + "s ";

			// If the countdown is over, stop updating and display a message
			if (timeRemaining < 0) {
				clearInterval(countdownInterval);
				document.getElementById("countdown").innerHTML = "Countdown over!";
			}
		}, 1000);
	</script>
</body>
</html
