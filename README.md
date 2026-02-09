# Para-romi
Página para romi
<!DOCTYPE html><html lang="es">
<head>
<meta charset="UTF-8">
<title>Romina, ¿quieres ser mi San Valentín?</title>
<style>
    body {
        font-family: 'Arial', sans-serif;
        background: linear-gradient(135deg, #a0c4ff, #4d79ff);
        color: #f0f0f0;
        text-align: center;
        padding-top: 50px;
        height: 100vh;
        overflow: hidden;
    }
    h1 {
        font-size: 3rem;
        color: #1e90ff;
        margin-bottom: 10px;
        text-shadow: 2px 2px #00000050;
    }
    p {
        font-size: 1.3rem;
        margin-bottom: 30px;
        color: #e0f7ff;
        text-shadow: 1px 1px #00000050;
    }
    .fecha {
        font-size: 1rem;
        color: #cce7ff;
        margin-bottom: 40px;
    }
    button {
        background-color: #ffffff;
        color: #1e90ff;
        padding: 15px 35px;
        border: none;
        font-size: 1.3rem;
        border-radius: 15px;
        cursor: pointer;
        margin: 10px;
        transition: 0.3s;
        box-shadow: 2px 2px 10px #00000050;
    }
    button:hover {
        transform: scale(1.1);
    }
    #noBtn {
        position: absolute;
        background-color: #cce7ff;
        color: #004080;
    }
    .corazon, .gatito {
        position: absolute;
        animation: flotar 5s infinite ease-in-out;
        opacity: 0.8;
    }
    .gatito {
        font-size: 25px;
    }
    @keyframes flotar {
        0% { transform: translateY(0); opacity: 0.7; }
        50% { transform: translateY(-50px); opacity: 1; }
        100% { transform: translateY(0); opacity: 0.7; }
    }
    audio {
        margin-top: 20px;
        outline: none;
    }
</style>
</head>
<body><h1>Romina, ¿quieres ser mi San Valentín? 💙</h1>
<p>Desde que empezamos a hablar el <span class="fecha">12/01/26</span>, no dejo de pensar en vos. Romina, ser tu San Valentín sería el mejor upgrade de mi corazón 💙 😍</p><button onclick="alert('¡Sabía que dirías que sí, Romina! 💙💙💙')">Sí</button> <button id="noBtn">No</button>

<div style="margin-top: 20px;">
  <iframe width="320" height="180"
    src="https://www.youtube.com/embed/8obld3JrBNM?autoplay=1&loop=1&playlist=8obld3JrBNM"
    title="YouTube video player"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen>
  </iframe>
</div><script>
    const noBtn = document.getElementById("noBtn");
    noBtn.addEventListener("mouseover", () => {
        noBtn.style.left = Math.random() * (window.innerWidth - 100) + "px";
        noBtn.style.top = Math.random() * (window.innerHeight - 50) + "px";
    });

    function crearCorazon() {
        const corazon = document.createElement("div");
        corazon.classList.add("corazon");
        corazon.innerHTML = "💙";
        corazon.style.left = Math.random() * window.innerWidth + "px";
        corazon.style.top = Math.random() * window.innerHeight + "px";
        corazon.style.fontSize = (20 + Math.random() * 40) + "px";
        document.body.appendChild(corazon);

        setTimeout(() => {
            corazon.remove();
        }, 5000);
    }

    function crearGatito() {
        const gatito = document.createElement("div");
        gatito.classList.add("gatito");
        gatito.innerHTML = "😻";
        gatito.style.left = Math.random() * window.innerWidth + "px";
        gatito.style.top = Math.random() * window.innerHeight + "px";
        document.body.appendChild(gatito);

        setTimeout(() => {
            gatito.remove();
        }, 5000);
    }

    setInterval(crearCorazon, 700);
    setInterval(crearGatito, 1200);
</script></body>
</html>
