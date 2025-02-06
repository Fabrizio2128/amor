<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invitación Especial</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #ffe6e6;
            height: 100vh; /* Asegura que el body ocupe toda la altura de la página */
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }
        .container {
            text-align: center;
            position: relative;
            padding: 20px;
            max-width: 100%;
            width: 400px; /* Ajustar el tamaño máximo para pantallas pequeñas */
        }
        .heart {
            font-size: 50px;
            cursor: pointer;
            color: red;
            transition: transform 0.3s;
        }
        .heart:hover {
            transform: scale(1.2);
        }
        .hidden {
            display: none;
        }
        img {
            width: 100%; /* Hacer que las imágenes del collage sean responsivas */
            margin-top: 20px;
            cursor: pointer;
            max-width: 150px; /* Limitar el tamaño de las imágenes */
            height: auto;
            border-radius: 10px;
        }
        .heart-animation {
            position: absolute;
            color: red;
            font-size: 30px;
            animation: float 5s linear; /* Cambiar la duración a 5 segundos */
        }
        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100vh); opacity: 0; }
        }
        .collage {
            display: grid;
            grid-template-columns: repeat(4, 1fr); /* 4 columnas */
            grid-gap: 10px;
            margin-top: 20px;
        }
        .collage img {
            width: 100%;
            height: auto;
            border-radius: 10px;
        }
        .options {
            margin-top: 20px;
            font-size: 30px;
        }
        .options button {
            margin: 10px;
            font-size: 20px;
            padding: 10px 20px;
            cursor: pointer;
            background-color: #ffcccc;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .options button:hover {
            background-color: #ff6666;
        }
        .thank-you {
            font-size: 40px;
            color: #ff3366;
            margin-top: 30px;
        }
        .thank-you-container {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        .thank-you-container img {
            width: 100px;
            height: auto;
            border-radius: 10px;
        }
        .impacto {
            color: red;
            font-size: 50px;
            font-weight: bold;
            animation: impacto 1s ease-in-out infinite alternate;
        }
        .impacto-heart {
            font-size: 60px;
            color: red;
            animation: impacto 1s ease-in-out infinite alternate;
        }
        @keyframes impacto {
            0% { transform: scale(1); }
            100% { transform: scale(1.3); }
        }
        /* Corazones flotantes en el fondo */
        .floating-hearts {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none; /* Evita que los corazones interfieran con la interacción */
            z-index: -1;
        }
        .floating-hearts span {
            position: absolute;
            font-size: 30px;
            color: red;
            animation: heartFloat 10s infinite;
        }
        @keyframes heartFloat {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100vh); opacity: 0; }
        }
        .crown {
            position: absolute;
            top: -50px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 60px;
            color: gold;
        }
    </style>
</head>
<body>
    <!-- Corazones flotantes en el fondo -->
    <div class="floating-hearts">
        <!-- Corazones que aparecerán flotando -->
        <span style="left: 10vw; animation-delay: 0s;">❤️</span>
        <span style="left: 20vw; animation-delay: 1s;">❤️</span>
        <span style="left: 30vw; animation-delay: 2s;">❤️</span>
        <span style="left: 40vw; animation-delay: 3s;">❤️</span>
        <span style="left: 50vw; animation-delay: 4s;">❤️</span>
        <span style="left: 60vw; animation-delay: 5s;">❤️</span>
        <span style="left: 70vw; animation-delay: 6s;">❤️</span>
        <span style="left: 80vw; animation-delay: 7s;">❤️</span>
    </div>

    <div class="container">
        <h1 id="heart-button" class="heart" onclick="mostrarMensaje()">❤️ Tócame mi amor ❤️</h1>
        <div id="mensaje" class="hidden">
            <h2 class="impacto">HOLA PRINCESA <span class="impacto-heart">❤️</span></h2>
            <p>Mi amor hola, espero estés muy bien. Hace varios días estuve pensando en la manera de darte un pequeño detalle por el día de San Valentín. Por esta razón es que me quemé el cerebro haciendo esto jaja. Solo quería hacerte recordar que se acerca un día muy bonito para los dos.</p>
            <img id="imagen" src="https://i.imgur.com/ekRMYBx.jpeg" alt="Imagen tuya" onclick="mostrarInvitacion()">
            <p id="flechas" class="hidden">⬆️ TÓCAME ⬆️</p>
        </div>
        <div id="invitacion" class="hidden">
            <h2 class="impacto">Princesa <span class="impacto-heart">❤️</span></h2>
            <p>Estás cordialmente invitada y obligada a ser mi San Valentín y pasar un día bonito para celebrar. Te amo ❤️</p>
            <div class="collage">
                <!-- Aquí van las 8 fotos del collage -->
                <img src="https://i.imgur.com/xNabmRO.jpeg" alt="Foto 1" onclick="continuarConPasoSiguiente()">
                <img src="https://i.imgur.com/L6MojiW.jpeg" alt="Foto 2" onclick="continuarConPasoSiguiente()">
                <img src="https://i.imgur.com/zz3uxtF.jpeg" alt="Foto 3" onclick="continuarConPasoSiguiente()">
                <img src="https://i.imgur.com/GhzFMIx.jpeg" alt="Foto 4" onclick="continuarConPasoSiguiente()">
                <img src="https://i.imgur.com/UUsAmN3.jpeg" alt="Foto 5" onclick="continuarConPasoSiguiente()">
                <img src="https://i.imgur.com/q3PGflJ.jpeg" alt="Foto 6" onclick="continuarConPasoSiguiente()">
                <img src="https://i.imgur.com/HFdt1N7.jpeg" alt="Foto 7" onclick="continuarConPasoSiguiente()">
                <img src="https://i.imgur.com/zYXJjlb.jpeg" alt="Foto 8" onclick="continuarConPasoSiguiente()">
            </div>
            <p id="flechas-collage" class="hidden">⬆️ Toca la foto que más te guste ⬆️</p>
        </div>
        <div id="opciones" class="hidden">
            <h2>¿Quieres ser mi San Valentín?</h2>
            <div class="options">
                <button onclick="elegirOpcion('si')">SI</button>
                <button onclick="elegirOpcion('si')">SI</button>
            </div>
        </div>
        <div id="gracias" class="hidden">
            <div class="thank-you-container">
                <div class="crown">👑</div> <!-- Corona de princesa encima de la imagen -->
                <p class="thank-you">GRACIAS POR ESCOGER, ERES UNA PRINCESA HERMOSA</p>
                <img src="https://i.imgur.com/CFQN9qE.jpeg" alt="Imagen de Princesa">
            </div>
        </div>
    </div>

    <script>
        function mostrarMensaje() {
            let heartButton = document.getElementById('heart-button');
            heartButton.style.display = 'none';
            for (let i = 0; i < 100; i++) { // Generar muchos más corazones flotando
                let heart = document.createElement('div');
                heart.classList.add('heart-animation');
                heart.innerHTML = '❤️';
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.top = Math.random() * 100 + 'vh';
                document.body.appendChild(heart);
                setTimeout(() => heart.remove(), 5000); // Duración de 5 segundos para los corazones
            }
            setTimeout(() => {
                document.getElementById('mensaje').classList.remove('hidden');
                document.getElementById('flechas').classList.remove('hidden');
            }, 5000);
        }

        function mostrarInvitacion() {
            document.getElementById('mensaje').classList.add('hidden'); // Ocultar el mensaje anterior
            document.getElementById('flechas').classList.add('hidden'); // Ocultar el texto de "TÓCAME"
            document.getElementById('invitacion').classList.remove('hidden'); // Mostrar la invitación
            document.getElementById('flechas-collage').classList.remove('hidden'); // Mostrar el texto de "Toca la foto que más te guste"
            crearCorazones(); // Crear corazones flotantes
        }

        function crearCorazones() {
            for (let i = 0; i < 5; i++) {
                let heart = document.createElement('div');
                heart.classList.add('heart-animation');
                heart.innerHTML = '❤️';
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.animation = `heartFloat ${Math.random() * 5 + 5}s infinite`; // Duración aleatoria
                document.body.appendChild(heart);
                setTimeout(() => heart.remove(), 10000); // Duración de 10 segundos para los corazones
            }
        }

        function continuarConPasoSiguiente() {
            document.getElementById('invitacion').classList.add('hidden');
            document.getElementById('opciones').classList.remove('hidden');
        }

        function elegirOpcion(opcion) {
            if (opcion === 'si') {
                document.getElementById('opciones').classList.add('hidden');
                document.getElementById('gracias').classList.remove('hidden');
            }
        }
    </script>
</body>
</html>
