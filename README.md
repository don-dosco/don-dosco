<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Viñedos Don Dosco</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }
        
        header {
            background-color: #800020;
            color: white;
            text-align: center;
            padding: 20px;
        }

        .slider {
            position: relative;
            max-width: 100%;
            margin: auto;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .slide {
            display: none;
        }

        .slide img {
            width: 100%;
            height: auto;
            border-radius: 10px;
        }

        .nav-buttons {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
        }

        .nav-button {
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .nav-button:hover {
            background-color: rgba(0, 0, 0, 0.8);
        }

        .catalogo, .promociones, .testimonios, .contacto {
            padding: 40px 20px;
            text-align: center;
            background-color: white;
            margin: 20px auto;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            max-width: 1200px;
        }

        h2 {
            color: #800020;
        }

        .vino-item {
            display: inline-block;
            margin: 20px;
            width: 280px;
            border: 1px solid #ccc;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
        }

        .vino-item:hover {
            transform: scale(1.05);
        }

        .vino-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .vino-item h3 {
            margin: 10px 0;
            color: #800020;
        }

        .vino-item p {
            padding: 0 10px;
        }

        .vino-item button {
            background-color: #800020;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            width: 100%;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .vino-item button:hover {
            background-color: #9a002b;
        }

        .promocion-item {
            display: inline-block;
            margin: 20px;
            width: 280px;
            border: 1px solid #ccc;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
        }

        .promocion-item:hover {
            transform: scale(1.05);
        }

        .promocion-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .carrito {
            position: fixed;
            top: 20px;
            right: 20px;
            background-color: #800020;
            color: white;
            padding: 10px;
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        .carrito-contenido {
            display: none;
            position: absolute;
            top: 50px;
            right: 0;
            background-color: white;
            border: 1px solid #ccc;
            border-radius: 10px;
            width: 200px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
            z-index: 1;
        }

        .carrito-contenido p {
            margin: 10px;
            color: #333;
        }

        .testimonio {
            margin: 20px 0;
            font-style: italic;
        }

        /* Responsividad */
        @media (max-width: 600px) {
            .vino-item, .promocion-item {
                width: 90%;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>Viñedos Don Dosco</h1>
        <p>La esencia de los mejores vinos de Argentina</p>
    </header>

    <div class="slider">
        <div class="slide">
            <img src="potos/uvas2.jpeg" alt="Slider Imagen 1">
        </div>
        <div class="slide">
            <img src="potos/valle 3.jpeg" alt="Slider Imagen 2">
        </div>
        <div class="slide">
            <img src="potos/bodega 3.jpeg" alt="Slider Imagen 3">
        </div>
        <div class="nav-buttons">
            <button class="nav-button" onclick="moveSlide(-1)">❮</button>
            <button class="nav-button" onclick="moveSlide(1)">❯</button>
        </div>
    </div>

    <section id="catalogo" class="catalogo">
        <h2>Catálogo de Vinos</h2>
        <div class="vino-item">
            <img src="potos/vino2.jpeg" alt="Vino Malbec">
            <h3>Malbec</h3>
            <p>Vino tinto con notas de frutas rojas y un toque de roble.</p>
            <button onclick="agregarAlCarrito('Malbec')">Agregar al Carrito</button>
        </div>
        <div class="vino-item">
            <img src="potos/caja2.jpeg" alt="Vino Cabernet Sauvignon">
            <h3>Cabernet Sauvignon</h3>
            <p>Un vino robusto con sabores intensos y un final suave.</p>
            <button onclick="agregarAlCarrito('Cabernet Sauvignon')">Agregar al Carrito</button>
        </div>
        <div class="vino-item">
            <img src="potos/caja3.jpeg" alt="Vino Syrah">
            <h3>Syrah</h3>
            <p>Vino con aroma de especias y un cuerpo elegante.</p>
            <button onclick="agregarAlCarrito('Syrah')">Agregar al Carrito</button>
        </div>
    </section>

    <section id="promociones" class="promociones">
        <h2>Promociones</h2>
        <div class="promocion-item">
            <img src="potos/caja4.jpeg" alt="Promoción Vino 1">
            <h3>30% de Descuento en Malbec</h3>
            <p>Solo por tiempo limitado.</p>
        </div>
        <div class="promocion-item">
            <img src="potos/promocion.jpeg" alt="Promoción Vino 2">
            <h3>2x1 en Cabernet Sauvignon</h3>
            <p>Aprovecha nuestra oferta especial.</p>
        </div>
        <div class="promocion-item">
            <img src="potos/pack.jpeg" alt="Promoción Vino 3">
            <h3>Descuento del 20% en la primera compra</h3>
            <p>Únete a nuestra familia de vinos.</p>
        </div>
    </section>

    <section id="testimonios" class="testimonios">
        <h2>Testimonios de Nuestros Clientes</h2>
        <div class="testimonio">
            <p>"El mejor vino que he probado, definitivamente volveré por más!" - Juan P.</p>
        </div>
        <div class="testimonio">
            <p>"Una experiencia increíble, el servicio es excelente." - Ana R.</p>
        </div>
        <div class="testimonio">
            <p>"Me encantó el sabor y la calidad. ¡Altamente recomendado!" - Luis M.</p>
        </div>
    </section>

    <div class="carrito" onclick="toggleCarrito()">
        🛒
    </div>
    <div class="carrito-contenido" id="carritoContenido">
        <h3>Productos en el Carrito</h3>
        <p id="carritoLista">No hay productos en el carrito.</p>
    </div>

    <section id="contacto" class="contacto">
        <h2>Contacto</h2>
        <p>Para más información, contáctanos en: <a href="mailto:info@donbosco.com">familiadondosco@gmail.com</a></p>
    </section>

    <script>
        let slideIndex = 0;
        showSlides();

        function showSlides() {
            const slides = document.getElementsByClassName("slide");
            for (let i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";
            }
            slideIndex++;
            if (slideIndex > slides.length) { slideIndex = 1 }
            slides[slideIndex - 1].style.display = "block";
            setTimeout(showSlides, 5000); // Cambiar cada 5 segundos
        }

        function moveSlide(n) {
            slideIndex += n - 1; // Ajustar el índice
            showSlides();
        }

        let carrito = [];

        function agregarAlCarrito(vino) {
            carrito.push(vino);
            actualizarCarrito();
        }

        function actualizarCarrito() {
            const listaCarrito = document.getElementById("carritoLista");
            if (carrito.length === 0) {
                listaCarrito.innerHTML = "No hay productos en el carrito.";
            } else {
                listaCarrito.innerHTML = carrito.join(", ");
            }
        }

        function toggleCarrito() {
            const contenido = document.getElementById("carritoContenido");
            contenido.style.display = contenido.style.display === "block" ? "none" : "block";
        }
    </script>
</body>
</html>
