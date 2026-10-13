<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mi página web</title>

<style>
:root {
    --azul: #1a7a4c;
    --oscuro: #142638;
    --fondo: #f6f3e8;
    --borde: #cbd3df;
}

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: var(--fondo);
    color: #2f3d2f;
}

header {
    background: var(--azul);
    color: white;
    padding: 20px;
}

.encabezado {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
}

header h1 {
    margin: 0;
    font-size: 25px;
}

nav {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 18px;
}

nav a {
    color: white;
    text-decoration: none;
    padding: 10px;
    border-radius: 5px;
}

nav a:hover {
    background: #1649c5;
}

#tema {
    border: none;
    background: white;
    color: var(--azul);
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
}

.contenedor {
    display: grid;
    grid-template-columns: 3fr 1fr;
    gap: 20px;
    padding: 20px;
}

.seccion {
    background: white;
    border: 2px dashed var(--borde);
    border-radius: 5px;
    padding: 12px;
    margin-bottom: 12px;
    scroll-margin-top: 15px;
}

.seccion h3 {
    margin: 0 0 10px;
    font-size: 16px;
    color: #344b69;
}

.resaltado {
    background: #ffe680;
    padding: 8px;
    display: inline-block;
}

table {
    width: 100%;
    border-collapse: collapse;
}

th {
    background: var(--azul);
    color: white;
}

td, th {
    border: 1px solid #aab4c2;
    padding: 4px;
    text-align: left;
}

.multimedia {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    align-items: center;
}

.foto {
    width: 100px;
    height: 80px;
    background: #91a1b9;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
}

video {
    width: 180px;
    max-width: 100%;
    background: black;
}

label {
    display: inline-block;
    width: 150px;
    margin: 6px 0;
}

input, select {
    max-width: 100%;
    width: 200px;
    padding: 5px;
    border: 1px solid #9ba8b9;
    border-radius: 3px;
}

#enviar {
    background: var(--azul);
    color: white;
    border: none;
    padding: 9px 18px;
    margin-top: 10px;
    border-radius: 5px;
    cursor: pointer;
}

aside {
    background: #dfe8ff;
    padding: 15px;
}

aside h3 {
    margin-top: 0;
}

details {
    background: white;
    padding: 10px;
    border: 1px dashed #aab4c2;
    margin-top: 20px;
}

footer {
    background: var(--oscuro);
    color: white;
    text-align: center;
    padding: 20px;
}

body.oscuro {
    --fondo: #17202b;
    --borde: #697789;
    color: #eeeeee;
}

body.oscuro .seccion {
    background: #253344;
}

body.oscuro .seccion h3 {
    color: white;
}

body.oscuro aside {
    background: #303f58;
}

body.oscuro details {
    background: #253344;
}

@media (max-width: 700px) {
    .contenedor {
        grid-template-columns: 1fr;
        padding: 12px;
    }

    header {
        padding: 15px;
    }

    label {
        width: 100%;
    }

    input, select {
        width: 100%;
    }
}
</style>
</head>

<body>

<header>
    <div class="encabezado">
        <h1>Mi página web</h1>
        <button id="tema" onclick="cambiarTema()">
            Cambiar tema
        </button>
    </div>

    <nav>
        <a href="#texto">Texto</a>
        <a href="#listas">Listas</a>
        <a href="#tabla">Tabla</a>
        <a href="#multimedia">Multimedia</a>
        <a href="#formulario">Formulario</a>
        <a href="#contacto">Contacto</a>
    </nav>
</header>

<div class="contenedor">

<main>

    <section class="seccion" id="multimedia">
        <h3>multimedia</h3>
        <p>
            Párrafo con <b>negrita</b>,
            <i>cursiva</i> y
            <mark>resaltado</mark>.
            Cita destacada.
            <a href="https://www.google.com"
               target="_blank">Enlace externo</a>.
        </p>
        <blockquote>
            Esta es una cita de ejemplo.
        </blockquote>
        <p class="resaltado">Texto resaltado</p>
    </section>

    <section class="seccion" id="listas">
        <h3>Listas</h3>

        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
        </ul>

        <ol>
            <li>Crear</li>
            <li>Escribir</li>
            <li>Publicar</li>
        </ol>

        <p>Lista de definiciones:</p>
        <dl>
            <dt><b>HTML</b></dt>
            <dd>Define la estructura de una página web.</dd>

            <dt><b>CSS</b></dt>
            <dd>Permite diseñar la página.</dd>
        </dl>
    </section>

    <section class="seccion" id="tabla">
        <h3>Tabla</h3>

        <table>
            <thead>
                <tr>
                    <th>Tecnología</th>
                    <th>Función</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>HTML</td>
                    <td>Estructura</td>
                </tr>
                <tr>
                    <td>CSS</td>
                    <td>Diseño</td>
                </tr>
                <tr>
                    <td>JavaScript</td>
                    <td>Interactividad</td>
                </tr>
            </tbody>
        </table>
    </section>

    <section class="seccion" id="multimedia">
        <h3>Multimedia</h3>

        <div class="multimedia">
            <figure>
                <div class="foto">FOTO</div>
                <figcaption>Pie de foto</figcaption>
            </figure>

            <video controls>
              <p>video de la naturaleza </p>
            </video>
        </div>
    </section>

    <section class="seccion" id="formulario">
        <h3>Formulario</h3>

        <form id="miFormulario">
            <label for="nombre">Nombre</label>
            <input type="text" id="nombre"
                   name="nombre" required>
            <br>

            <label for="correo">Correo</label>
            <input type="email" id="correo"
                   name="correo" required>
            <br>

            <label for="pais">País (lista desplegable)</label>
            <select id="pais" name="pais" required>
                <option value="">Selecciona un país</option>
                <option value="México">México</option>
                <option value="Guatemala">Guatemala</option>
                <option value="Colombia">Colombia</option>
                <option value="España">España</option>
            </select>
            <br>

            <button type="submit" id="enviar">Enviar</button>
        </form>

        <p id="resultado"></p>
    </section>

</main>

<aside>
    <h3>Barra lateral</h3>
    <p>Contenido relacionado</p>

    <details>
        <summary>Desplegable</summary>
        <p>¡Aquí puedes colocar más contenido!</p>
        <p>HTML, CSS y JavaScript permiten crear páginas web.</p>
    </details>
</aside>

</div>

<footer id="contacto">
    <p>© 2026 Tu Nombre. Hecho con HTML, CSS y JavaScript.</p>
    <p>Contacto: ejemplo@correo.com</p>
</footer>

<script>
function cambiarTema() {
    document.body.classList.toggle("oscuro");
}

document.getElementById("miFormulario").addEventListener(
    "submit", function(event) {
        event.preventDefault();

        const nombre = document.getElementById("nombre").value;
        const correo = document.getElementById("correo").value;
        const pais = document.getElementById("pais").value;

        document.getElementById("resultado").textContent =
            "Nombre: " + nombre +
            " | Correo: " + correo +
            " | País: " + pais;
    }
);
</script>

</body>
</html>
