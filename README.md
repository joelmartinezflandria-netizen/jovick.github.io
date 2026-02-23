<!DOCTYPE html>
<html>
<head>
    <title>Joel ❤️ Vicky</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            color: white;
        }
        #countdown {
            font-size: 30px;
            margin-top: 20px;
        }
        img {
            width: 200px;
            border-radius: 15px;
            margin: 10px;
        }
    </style>
</head>
<body>

<h1>Joel ❤️ Vicky</h1>
<h2>Falta para vernos:</h2>
<div id="countdown"></div>

<h2>Nosotros</h2>
<img src="foto1.jpg">
<img src="foto2.jpg">

<script>
    let nextDate = new Date("2026-02-24T13:30:00").getTime();

    let countdown = setInterval(function() {
        let now = new Date().getTime();
        let distance = nextDate - now;

        let days = Math.floor(distance / (1000 * 60 * 60 * 24));
        let hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));

        document.getElementById("countdown").innerHTML =
            days + " días " + hours + " horas " + minutes + " minutos";

        if (distance < 0) {
            clearInterval(countdown);
            document.getElementById("countdown").innerHTML = "Ya nos estamos viendo ❤️";
        }
    }, 1000);
</script>

</body>
</html>
