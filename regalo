<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cartita para mi VV</title>
    <style>
        body {
            background-image: url('https://i.pinimg.com/564x/e1/41/db/e141db1c545243a1294e92d686df443b.jpg'); /* Fondo original */
            background-size: cover; /* Para cubrir toda la pantalla */
            background-position: center; /* Centrar la imagen */
            font-family: 'Arial', sans-serif;
            text-align: center;
            padding: 20px;
            color: #fff; /* Color del texto */
        }
        h1 {
            font-size: 48px; /* Tamaño más grande */
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.7); /* Sombra del texto */
            margin-bottom: 20px;
        }
        .corazon {
            color: #ff1493; /* Color del corazón */
            font-size: 28px;
            margin-top: 10px;
            animation: pulse 1s infinite; /* Animación de pulso */
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        #botonApreta {
            background-color: #ff0000; /* Color rojo */
            color: white;
            border: none;
            border-radius: 10px; /* Esquinas redondeadas */
            padding: 20px 40px; /* Tamaño más grande */
            font-size: 24px; /* Tamaño de fuente más grande */
            cursor: pointer;
            transition: background-color 0.3s;
            font-weight: bold; /* Negrita */
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3); /* Sombra del botón */
            margin-top: 20px;
        }
        #botonIniciarMusica {
            background-color: #ff69b4; /* color rosado */
            color: white;
            border: none;
            border-radius: 5px;
            padding: 15px 30px;
            font-size: 20px;
            cursor: pointer;
            transition: background-color 0.3s;
            margin-top: 20px;
            font-weight: bold; /* Negrita */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Sombra del botón */
        }
        #botonPorQue, #botonSiguiente, #botonVerVida, #botonAtras {
            background-color: #ff69b4; /* color rosado */
            color: white;
            border: none;
            border-radius: 5px;
            padding: 15px 30px;
            font-size: 20px;
            cursor: pointer;
            transition: background-color 0.3s;
            margin-top: 20px;
            font-weight: bold; /* Negrita */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Sombra del botón */
        }
        #botonPorQue:hover, #botonSiguiente:hover, #botonVerVida:hover, #botonAtras:hover, #botonIniciarMusica:hover {
            background-color: #ff1493; /* rosado más oscuro */
        }
        #mensajePorQue {
            display: none;
            margin-top: 20px;
            font-size: 20px;
            animation: fadeIn 1s;
            background-color: rgba(255, 255, 255, 0.8); /* Fondo blanco semi-transparente */
            color: black; /* Color del texto */
            padding: 15px;
            border-radius: 10px; /* Esquinas redondeadas */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Sombra */
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        #paginaSiguiente {
            display: none; /* Ocultar inicialmente */
            background-color: rgba(255, 255, 255, 0.9); /* Fondo blanco */
            color: black; /* Color del texto */
            padding: 20px;
            border-radius: 10px; /* Esquinas redondeadas */
            margin-top: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Sombra */
        }
        #vidaConVos {
            display: none; /* Ocultar inicialmente */
            background-color: rgba(0, 0, 0, 0.8); /* Fondo negro semi-transparente */
            color: white; /* Color del texto */
            padding: 20px;
            border-radius: 10px; /* Esquinas redondeadas */
            margin-top: 20px;
        }
    </style>
    <script>
        let audio;

        function iniciarMusica() {
            audio = new Audio("https://rr4---sn-bg0eznz7.googlevideo.com/videoplayback?expire=1724140464&ei=UPfDZtrUDvmb1sQPhcLIgA0&ip=189.28.81.242&id=o-AMEWbTUatFAlePjZqFJoGvAYoZOJB3lEKmYKxlX6kU2k&itag=251&source=youtube&requiressl=yes&xpc=EgVo2aDSNQ%3D%3D&gcr=bo&bui=AQmm2ezQnf3gVpfQvnAjotWtmILG_J-QHztREl8alBKZAvA7YS01_BLuhRs5LglWlC5sYCF1flzJX3pg&spc=Mv1m9k3fY-sx8hpgVCmcdMrvGhEnCCfejCIyZBLfikPtW5QfM3U8&vprv=1&svpuc=1&mime=audio%2Fwebm&ns=Tdt7_EsF4XFwLG_XvLQIG-cQ&rqh=1&gir=yes&clen=3151776&dur=175.281&lmt=1714789371709430&keepalive=yes&c=WEB_CREATOR&sefc=1&txp=5432434&n=tGHztP3_MYa1qg&sparams=expire%2Cei%2Cip%2Cid%2Citag%2Csource%2Crequiressl%2Cxpc%2Cgcr%2Cbui%2Cspc%2Cvprv%2Csvpuc%2Cmime%2Cns%2Crqh%2Cgir%2Cclen%2Cdur%2Clmt&sig=AJfQdSswRAIgcjjWi3xMjJ-E1454bu-f-LbXKybVToPKCrfi6ZKQLG0CIFIkk4VNn-ZokKeE8BaD1ivopM8-Re5KVQm7gwV3JhhL&rm=sn-upbvcv-jccl7l,sn-njaes76&rrc=79,104&fexp=24350516,24350518,24350556,24350561&req_id=e50e291c3a73a3ee&redirect_counter=2&cms_redirect=yes&cmsv=e&ipbypass=yes&mh=Cj&mip=189.28.76.210&mm=29&mn=sn-bg0eznz7&ms=rdu&mt=1724118612&mv=m&mvi=4&pl=24&lsparams=ipbypass,mh,mip,mm,mn,ms,mv,mvi,pl&lsig=AGtxev0wRQIgYVAhGMynD-jUEPYe4rTdkwsrIFDsFsgtBNEcsgfO1E8CIQCj6tqeGZYd1ucT9lNEEp4qMbOVo6ejP_vNAjEdWwwiMA%3D%3D");
            audio.loop = true; // Repetir música
            audio.play(); // Iniciar la música
        }

        function mostrarMensaje() {
            document.body.innerHTML = 
                <h1>Cada día a tu lado es un nuevo capítulo en nuestra historia de amor, y no puedo esperar a escribir muchos más con vos. 💖</h1>
                <div class="corazon">Te quiero muxo ❤️</div>
                <button id="botonPorQue" onclick="mostrarPorQue()">Pero, ¿Por qué? 🤔</button>
                <div id="mensajePorQue">Te quiero porque sabes cómo hacer que hasta los días grises brillen, porque soportas mis rarezas, y porque en cada sonrisa tuya encuentro mi lugar favorito. 🌈</div>
                <button id="botonSiguiente" onclick="irASiguiente()">Siguiente ➡️</button>
                <div id="paginaSiguiente">
                    <h2>Mi Vida sin Vos</h2>
                    <div id="mensaje1">¿Sabes cómo sería mi vida sin vos? 🤷‍♂️</div>
                    <div id="mensaje2">Así como esta página en blanco. 📄</div>
                    <button id="botonVerVida" onclick="mostrarVidaConVos()">Ahora mira mi vida con vos en ella ❤️</button>
                    <button id="botonAtras" onclick="volver()">Atrás 🔙</button>
                </div>
                <div id="vidaConVos" style="display:none;">
                    <h1>Así de hermosa sería 🌟</h1>
                    <p>Desde que llegaste, cada día es un regalo lleno de amor y alegría. 🎁</p>
                    <p>Te quiero mucho ❤️</p>
                    <button id="botonAtras" onclick="volver()">Atrás 🔙</button>
                </div>
            ;
        }

        function mostrarPorQue() {
            document.getElementById('mensajePorQue').style.display = 'block';
        }

        function irASiguiente() {
            document.getElementById('paginaSiguiente').style.display = 'block'; // Mostrar la nueva sección
            mostrarMensajes(); // Llamar a la función para mostrar los mensajes
        }

        function mostrarMensajes() {
            const mensaje1 = document.getElementById('mensaje1');
            const mensaje2 = document.getElementById('mensaje2');
            const botonVerVida = document.getElementById('botonVerVida');

            // Mostrar el primer mensaje
            setTimeout(() => {
                mensaje1.style.display = 'block';
            }, 1000); // Aparece después de 1 segundo

            // Mostrar el segundo mensaje
            setTimeout(() => {
                mensaje2.style.display = 'block';
            }, 3000); // Aparece después de 3 segundos

            // Mostrar el botón
            setTimeout(() => {
                botonVerVida.style.display = 'block';
            }, 5000); // Aparece después de 5 segundos
        }

        function mostrarVidaConVos() {
            document.getElementById('paginaSiguiente').style.display = 'none'; // Ocultar la sección anterior
            document.getElementById('vidaConVos').style.display = 'block'; // Mostrar la nueva sección
            document.body.style.backgroundImage = "url('https://i.pinimg.com/564x/e9/c1/79/e9c179b336e63ad1aec9ab74187e125d.jpg')"; // Cambiar fondo
        }

        function volver() {
            document.body.innerHTML = 
                <h1>Cartita para mi VV</h1>
                <button id="botonApreta" onclick="mostrarMensaje()">Apreta aquí 🌟</button>
                <button id="botonIniciarMusica" onclick="iniciarMusica()">Iniciar Música 🎶</button>
            ;
        }

        window.onload = function() {
            document.getElementById('botonIniciarMusica').onclick = iniciarMusica; // Asignar el evento al botón
        };
    </script>
</head>
<body>
    <h1>Cartita para mi VV</h1>
    <button id="botonApreta" onclick="mostrarMensaje()">Apreta aquí 🌟</button>
    <button id="botonIniciarMusica" onclick="iniciarMusica()">Iniciar Música 🎶</button>
</body>
</html>
