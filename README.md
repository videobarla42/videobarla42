<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Carrusel de Imágenes</title>
<style>
    body {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
    }
    .carousel-container {
        text-align: center;
        position: relative;
        width: 80%;
        margin: auto;
        overflow: hidden; /* Oculta las miniaturas que estén fuera del contenedor */
    }
    .main-image {
        max-width: 100%;
        height: auto;
    }
    .thumbnail-images {
        margin-top: 20px;
        white-space: nowrap; /* Para que las miniaturas no se rompan en varias líneas */
        animation: moveThumbnails 80s linear infinite; /* Animación para mover las miniaturas */
    }
    .thumbnail-images img {
        width: 100px; /* Tamaño de las miniaturas */
        height: auto;
        margin: 0 5px;
        cursor: pointer;
        border: 2px solid transparent;
        transition: border-color 0.3s ease;
    }
    .thumbnail-images img:hover {
        border-color: #333; /* Color del borde al pasar el ratón */
    }

    @keyframes moveThumbnails {
        0% {
            transform: translateX(0);
        }
        100% {
            transform: translateX(calc(-100% - 10px)); /* Se desplaza una miniatura más allá del contenedor */
        }
    }

    @keyframes moveThumbnailsForward {
        0% {
            transform: translateX(0);
        }
        100% {
            transform: translateX(calc(-100% - 10px)); /* Mueve las miniaturas hacia adelante */
        }
    }

    @keyframes moveThumbnailsBackward {
        0% {
            transform: translateX(0);
        }
        100% {
            transform: translateX(calc(100% + 10px)); /* Mueve las miniaturas hacia atrás */
        }
    }

    #formulario {
    margin-top: 20px;
}

#confirmar-compra-btn {
    margin-top: 10px;
}


#formulario-compra {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 80%;
    max-width: 600px; /* Opcional: establece un ancho máximo para evitar que el formulario sea demasiado ancho en pantallas grandes */
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}





</style>
</head>
<body>
<h1>envios contra entrega para bucaramanga y su area metropolitana</h1>
    <div class="carousel-container">
        <h2>pidelo ahora y paga en la puerta de tu casa</h2>
        <button class="prev-button">&lt;</button>
        <img class="main-image" src="imagenes/(1)DS-2CE56D0T-IRPF.jpg" alt="Imagen Principal">
        <button class="next-button">&gt;</button>
        <div class="thumbnail-images">
            <img src="imagenes/(138)DS-2CE10DF0T-PFS.png" alt="Miniatura 1">
            <img src="imagenes/(138)DS-2CE10DF0T-PFS.png" alt="Miniatura 2">
            <img src="imagenes/(138)DS-2CE10DF0T-PFS.png" alt="Miniatura 3">
            <img src="imagenes/(138)DS-2CE10DF0T-PFS.png" alt="Miniatura 4">
            <img src="imagenes/(138)DS-2CE10DF0T-PFS.png" alt="Miniatura 5">
            <img src="imagenes/(138)DS-2CE10DF0T-PFS.png" alt="Miniatura 6">
            <img src="imagenes/(1)DS-2CE56D0T-IRPF.jpg" alt="Miniatura 7">
        </div>
    </div>
    <h2>1111</h2>
    <p>2222</p>
    <h2>3333</h2>
    <p>4444</p>

    <button id="comprar-btn">Comprar</button>

    

    <div id="formulario-compra" style="display: none;">
        <div class="col-12 col-sm-6 col-md-4 col-lg-3 col-xl-2 mb-4">
            <div class="form-container">
                <h2 class="text-center mb-4">Para realizar la compra, por favor ingrese los datos completos en el formulario para poder hacer llegar la cámara a su domicilio. El envío es completamente gratis y recibe una memoria micro SD adicional por la compra, con un valor de $259,919 pesos. Por favor, recuerde que el pedido es contraentrega y es fundamental que cuente con el dinero a la mano para poder hacerle la entrega.</h2>
                <form id="myForm">
                    <div class="form-group">
                        <label for="nombreCompleto">Nombre Completo:</label>
                        <input type="text" class="form-control" id="nombreCompleto" name="nombreCompleto" required>
                    </div>
                    <div class="form-group">
                        <label for="telefono">Teléfono:</label>
                        <input type="tel" class="form-control" id="telefono" name="telefono" required>
                    </div>
                    <div class="form-group">
                        <label for="direccionBarrio">Dirección/Barrio:</label>
                        <input type="text" class="form-control" id="direccionBarrio" name="direccionBarrio" required>
                    </div>
                    <div class="form-group">
                        <label for="ciudadDepartamento">Ciudad/Departamento:</label>
                        <input type="text" class="form-control" id="ciudadDepartamento" name="ciudadDepartamento" required>
                    </div>
                    <div class="form-group">
                        <label for="correoElectronico">Correo Electrónico:</label>
                        <input type="email" class="form-control" id="correoElectronico" name="correoElectronico" required>
                    </div>
                    <!-- Botón de apertura de la ventana modal -->
                        <button type="button" class="btn btn-primary btn-block custom-btn" onclick="validarYEnviar(); fbq('track', 'Purchase');">confirmar compra</button>
                </form>
            </div>
        </div>
    </div>


    





    
<footer>s24seguridadelectronica</footer>

<script>
    function enviarDatos() {
    var nombreCompleto = document.getElementById("nombreCompleto").value;
    var telefono = document.getElementById("telefono").value;
    var direccionBarrio = document.getElementById("direccionBarrio").value;
    var ciudadDepartamento = document.getElementById("ciudadDepartamento").value;
    var correoElectronico = document.getElementById("correoElectronico").value;

    var formData = new FormData();
    formData.append("nombreCompleto", nombreCompleto);
    formData.append("telefono", telefono);
    formData.append("direccionBarrio", direccionBarrio);
    formData.append("ciudadDepartamento", ciudadDepartamento);
    formData.append("correoElectronico", correoElectronico);

    fetch('https://script.google.com/macros/s/AKfycbwd5Ne_B5sPStA1KHNPm390zcBubpNJWyBBtu8dzI88rbdg9CPYsy-cXEPs2wqB6nix-A/exec', {
        method: 'POST',
        body: formData
    })
    .then(response => {
        if (response.ok) {
            // Mostrar un mensaje de confirmación
            alert('¡Datos enviados correctamente! ¡Gracias por su Compra en 3 dias habiles llegara su pedido!');
            // Limpiar el formulario después de enviar
            document.getElementById("myForm").reset();

            // Opcional: realizar otras acciones después de una compra exitosa

        } else {
            // Mostrar un mensaje de error si la respuesta del servidor no es exitosa
            alert('Error al enviar los datos');
        }
    })
    .catch(error => {
        console.error('Error:', error);
        // Mostrar un mensaje de error si hay un error en la solicitud
        alert('Error al enviar los datos');
    });
}
</script>




<script>
    function validarYEnviar() {
        var nombreCompleto = document.getElementById("nombreCompleto").value;
        var telefono = document.getElementById("telefono").value;
        var direccionBarrio = document.getElementById("direccionBarrio").value;
        var ciudadDepartamento = document.getElementById("ciudadDepartamento").value;
        var correoElectronico = document.getElementById("correoElectronico").value;

        // Verificar si algún campo está vacío
        if (nombreCompleto === "" || telefono === "" || direccionBarrio === "" || ciudadDepartamento === "" || correoElectronico === "") {
            alert("Por favor completa todos los campos antes de enviar el formulario.");
        } else {
            // Si todos los campos están llenos, llamar a la función para enviar los datos
            enviarDatos();
        }
    }
</script>



    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const mainImage = document.querySelector('.main-image');
            const thumbnails = document.querySelectorAll('.thumbnail-images img');
            const prevButton = document.querySelector('.prev-button');
            const nextButton = document.querySelector('.next-button');
            let currentIndex = 0;
    
            // Función para mostrar la imagen correspondiente al índice dado
            function showImage(index) {
                mainImage.src = thumbnails[index].src;
            }
    
            // Manejadores de eventos para los botones prev y next
            prevButton.addEventListener('click', function() {
                currentIndex = (currentIndex - 1 + thumbnails.length) % thumbnails.length;
                showImage(currentIndex);
            });
    
            nextButton.addEventListener('click', function() {
                currentIndex = (currentIndex + 1) % thumbnails.length;
                showImage(currentIndex);
            });
    
            // Manejador de eventos para hacer clic en miniaturas
            thumbnails.forEach((thumbnail, index) => {
                thumbnail.addEventListener('click', function() {
                    // Intercambiar src de la miniatura clicada con la imagen principal
                    let tempSrc = mainImage.src;
                    mainImage.src = thumbnail.src;
                    thumbnail.src = tempSrc;
                });
            });
    
            // Añadir soporte para eventos táctiles en dispositivos móviles
            thumbnails.forEach((thumbnail, index) => {
                thumbnail.addEventListener('touchstart', function() {
                    // Intercambiar src de la miniatura clicada con la imagen principal
                    let tempSrc = mainImage.src;
                    mainImage.src = thumbnail.src;
                    thumbnail.src = tempSrc;
                });
            });
        });

        document.addEventListener("DOMContentLoaded", function() {
    const comprarBtn = document.getElementById("comprar-btn");
    const formularioCompra = document.getElementById("formulario-compra");
    const confirmarCompraBtn = document.getElementById("confirmar-compra-btn");

    comprarBtn.addEventListener("click", function() {
        if (formularioCompra.style.display === "block") {
            formularioCompra.style.display = "none"; // Si está visible, se oculta
        } else {
            formularioCompra.style.display = "block"; // Si está oculto, se muestra
        }
    });

    confirmarCompraBtn.addEventListener("click", function() {
    // Aquí puedes agregar la lógica para procesar la compra

    // Se pueden obtener los valores de los campos del formulario
    var nombreCompleto = document.getElementById("nombreCompleto").value;
    var telefono = document.getElementById("telefono").value;
    var direccionBarrio = document.getElementById("direccionBarrio").value;
    var ciudadDepartamento = document.getElementById("ciudadDepartamento").value;
    var correoElectronico = document.getElementById("correoElectronico").value;

    // Aquí se puede agregar la lógica para enviar estos datos a un servidor
    // Por ejemplo, utilizando Fetch API para hacer una solicitud POST al servidor

    // Mostrar un mensaje de confirmación al usuario
    alert("¡Compra confirmada!");

    // Reiniciar el formulario después de la confirmación
    document.getElementById("myForm").reset();

    // Ocultar el formulario después de la confirmación
    formularioCompra.style.display = "none";
});
});


    </script>
    
    





</body>
</html>
