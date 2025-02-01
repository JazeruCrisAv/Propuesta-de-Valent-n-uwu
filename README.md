# Para mi amorcito
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>¡Sé mi Valentín!</title>
  <style>
    /* Estilos generales */
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      overflow: hidden;
      font-family: 'Quicksand', sans-serif;
      color: white;
      text-align: center;
    }

    /* Fondo animado como un amanecer */
    #propuesta {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(-45deg, #ff7e5f, #feb47b, #ff6a6a, #ffcccb, #ff7e5f);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
    }

    /* Animación del fondo */
    @keyframes gradientBG {
      0% {
        background-position: 0% 50%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 50%;
      }
    }

    /* Contenedor del mensaje */
    .container {
      background: rgba(0, 0, 0, 0.5);
      padding: 40px;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
      max-width: 600px;
    }

    /* Título */
    h1 {
      font-size: 4rem;
      margin-bottom: 20px;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
      font-weight: 300;
    }

    /* Mensaje */
    p {
      font-size: 2rem;
      margin-bottom: 30px;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
      font-weight: 300;
    }

    /* Botón */
    button {
      padding: 15px 30px;
      font-size: 1.5rem;
      border: none;
      border-radius: 5px;
      background: #ff4d4d;
      color: white;
      cursor: pointer;
      transition: background 0.3s ease;
      font-family: 'Quicksand', sans-serif;
      font-weight: 500;
    }

    button:hover {
      background: #ff1a1a;
    }

    /* Sección de agradecimiento (oculta inicialmente) */
    #agradecimiento {
      display: none;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(-45deg, #ff7e5f, #feb47b, #ff6a6a, #ffcccb, #ff7e5f);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      position: relative;
      overflow: hidden;
    }

    /* Corazones animados */
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: #ff4d4d;
      transform: rotate(-45deg);
      animation: float 5s infinite ease-in-out;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: #ff4d4d;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      top: 0;
      left: 10px;
    }

    @keyframes float {
      0% {
        transform: translateY(0) rotate(-45deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) rotate(-45deg);
        opacity: 0;
      }
    }
  </style>
  <!-- Fuente moderna y suave de Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500&display=swap" rel="stylesheet">
</head>
<body>
  <!-- Sección de la propuesta -->
  <section id="propuesta">
    <div class="container">
      <h1>¡Hola mi amor!</h1>
      <p>
        Este 14 de febrero, quiero que seas mi Valentín.<br>
        Eres lo más especial en mi vida y no puedo imaginar un día sin ti.<br>
        ¿Aceptas ser mi Valentín?<br>
        Con todo mi amor,<br>
        <strong>[Tu nombre]</strong>
      </p>
      <button onclick="mostrarAgradecimiento()">¡Acepto!</button>
    </div>
  </section>

  <!-- Sección de agradecimiento -->
  <section id="agradecimiento">
    <div class="container">
      <h1>¡Gracias por aceptar!</h1>
      <p>Eres el amor de mi vida. ❤️</p>
    </div>
    <!-- Corazones animados -->
    <div class="heart" style="top: 10%; left: 20%; animation-delay: 0s;"></div>
    <div class="heart" style="top: 20%; left: 50%; animation-delay: 1s;"></div>
    <div class="heart" style="top: 30%; left: 80%; animation-delay: 2s;"></div>
    <div class="heart" style="top: 50%; left: 10%; animation-delay: 3s;"></div>
    <div class="heart" style="top: 60%; left: 40%; animation-delay: 4s;"></div>
    <div class="heart" style="top: 70%; left: 70%; animation-delay: 5s;"></div>
    <div class="heart" style="top: 90%; left: 30%; animation-delay: 6s;"></div>
    <div class="heart" style="top: 80%; left: 60%; animation-delay: 7s;"></div>
  </section>

  <script>
    function mostrarAgradecimiento() {
      // Oculta la sección de la propuesta
      document.getElementById('propuesta').style.display = 'none';
      // Muestra la sección de agradecimiento
      document.getElementById('agradecimiento').style.display = 'flex';
    }
  </script>
</body>
</html>
