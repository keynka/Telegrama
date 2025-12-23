<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>💖 Un correo para ti 💖</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: "Poppins", sans-serif;
      background-color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      text-align: center;
      color: #333;
      transition: background-color 0.5s ease;
    }
    h2 {
      margin-bottom: 20px;
    }
    .screen {
      display: none;
      animation: fadeIn 0.8s ease;
      width: 90%;
      max-width: 600px;
    }
    .active {
      display: block;
    }
    .main-img {
      width: 280px;
      height: auto;
      margin-bottom: 15px;
      cursor: pointer;
      transition: transform 0.3s ease;
      border: none;
      box-shadow: none;
    }
    .main-img:hover {
      transform: scale(1.05);
    }
    .card {
      background: repeating-linear-gradient(
        white,
        white 28px,
        #e3e3e3 29px
      );
      border-radius: 0; /* esquinas en punta */
      padding: 40px 60px;
      border: 2px solid #e5e5e5;
      width: 95%;
      max-width: 900px;
      text-align: left;
      margin: 0 auto;
      box-sizing: border-box;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
      animation: fadeIn 1s ease;
    }
    .card h3 {
      font-family: 'Dancing Script', cursive;
      font-size: 2em;
      text-align: left;
      margin-bottom: 20px;
      margin-left: 10px;
      color: #444;
    }
    .card p {
      font-family: 'Dancing Script', cursive;
      font-size: 1.3em;
      line-height: 1.6;
      text-align: justify;
      color: #444;
      margin: 10px 0;
    }
    .return-btn {
      margin-top: 25px;
      padding: 10px 20px;
      font-size: 1em;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      transition: 0.3s;
      background-color: #ff4f81;
      color: white;
    }
    .return-btn:hover {
      background-color: #ff2a66;
    }
    @keyframes fadeIn {
      from {opacity: 0; transform: scale(0.95);}
      to {opacity: 1; transform: scale(1);}
    }
  </style>
</head>
<body>
  <div class="screen active" id="screen1">
    <h2>Hola, te llegó un correo</h2>
    <img src="https://acortar.link/799ZCM" onclick="nextScreen(2)">
  </div>
  <div class="screen" id="screen2">
    <h2>Una cartita para ti</h2>
    <img src="https://acortar.link/xL3lp1" onclick="nextScreen(3)">
  </div>
  <div class="screen" id="screen3">
    <h2>¡Ábrelo!</h2>
    <img src="https://acortar.link/0dF85N" onclick="nextScreen(4)">
  </div>
  <div class="screen" id="screen4">
    <h2>¿Qué dirá?</h2>
    <img src="https://acortar.link/UbWK9s"main-img" onclick="nextScreen(5)">
  </div>
  <div class="screen" id="screen5">
    <div class="card">
      <h3>Mi Princesa</h3>
      <p>No sé muy bien cómo empezar esta carta, pero aqui
        estoy alguien que solo ha diseñado viendo rapido un
        video de como se pograma esta cosa ajsjajsja espero
        te guste. Desde que nos hemos vuelto a reencontrar se
        que lo dije muchas veces pero nuestras vidas se han
        iluminado y llenado de amor de una forma sorprendente.</p>
      <p>Me gusta la forma en que hablas, tu hermosa voz tambien tu
        tierna risa que se te sale con ganas, y esa tranquilidad
        que transmitimos mutuamente. A veces pienso
        en ti sin motivo, solo porque sí, y de verdad te juro que
        es increible contigo haya sentido por primera vez se podria
        decir el amor verdadero y puro.</p>
      <p>Eres alguien especial para mí. Que te valoro, 
        te admiro y, sobre todo, te tengo un cariño enorme.</p>
      <p>Con mucho amor</p>
      <p>Tu caballero Julio 💌</p>
    </div>
    <div style="text-align: center;">
      <button class="return-btn" onclick="nextScreen(1)">🔙 Regresar</button>
    </div>
  </div>
  <script>
    function nextScreen(num) {
      const current = document.querySelector(".screen.active");
      if (current) current.classList.remove("active");
      document.getElementById("screen" + num).classList.add("active");
    }
  </script>
</body>
</html>
