<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechFix - Reparación de Móviles</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background-color: #f5f5f5;
            color: #333;
        }
        header {
            background: #000;
            color: white;
            padding: 50px 20px;
            font-size: 24px;
        }
        section {
            margin: 50px 20px;
        }
        .btn {
            display: inline-block;
            padding: 10px 20px;
            background: #000;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 20px;
        }
        form {
            max-width: 400px;
            margin: auto;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        input, textarea, button {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background: #000;
            color: white;
            cursor: pointer;
        }
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        .social-icons a {
            font-size: 24px;
            color: #000;
            text-decoration: none;
        }
    </style>
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>
<body>
    <header>
        <h1>TechFix</h1>
        <p>"Repara hoy, disfruta siempre."</p>
    </header>
    
    <section>
        <h2>Quiénes Somos</h2>
        <p id="quienesSomos"></p>
    </section>

    <section>
        <h2>Qué Ofrecemos</h2>
        <p id="queOfrecemos"></p>
    </section>

    <section>
        <h2>Contacto</h2>
        <form id="contactForm">
            <input type="text" id="nombre" placeholder="Nombre" required>
            <input type="email" id="email" placeholder="Correo Electrónico" required>
            <textarea id="mensaje" placeholder="Mensaje" required></textarea>
            <button type="submit">Enviar</button>
        </form>
        <p id="respuesta"></p>
    </section>
    
    <section class="social-icons">
        <a href="https://wa.me/50371351856" target="_blank"><i class="fab fa-whatsapp"></i></a>
        <a href="https://www.instagram.com/tech.fix503" target="_blank"><i class="fab fa-instagram"></i></a>
    </section>
    
    <script>
        // Agregar contenido dinámico con JavaScript
        document.getElementById("quienesSomos").innerText = 
            "Soy un microempresario graduado en electricidad y electrónica con pasión por reparar dispositivos electrónicos. " +
            "En TechFix, nos dedicamos a brindar soluciones rápidas y confiables para tus dispositivos. Nuestra experiencia y compromiso " +
            "nos convierten en tu mejor opción para reparaciones.";

        document.getElementById("queOfrecemos").innerText = 
            "Reparamos teléfonos móviles, laptops y otros dispositivos electrónicos. Ofrecemos diagnósticos precisos y " +
            "soluciones efectivas con garantía de calidad.";

        // Formulario de contacto dinámico
        document.getElementById("contactForm").addEventListener("submit", function(event) {
            event.preventDefault();
            const nombre = document.getElementById("nombre").value;
            const email = document.getElementById("email").value;
            const mensaje = document.getElementById("mensaje").value;
            
            if (nombre && email && mensaje) {
                document.getElementById("respuesta").innerText = "Gracias, " + nombre + ". Hemos recibido tu mensaje.";
            } else {
                document.getElementById("respuesta").innerText = "Por favor, completa todos los campos.";
            }
        });
    </script>
</body>
</html>
