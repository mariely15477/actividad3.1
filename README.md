Esta actividad esta compuesta por: 
index.html, style.css y add.html. 
El archivo index.html es una página web que muestra cuatro recetas de cocina diferentes. 
La página tiene un encabezado con un título y un menú de navegación que permite al usuario 
acceder a una página para agregar nuevas recetas. Cada receta se muestra en un cuadro separado 
que contiene un título, una imagen o video, una lista de ingredientes y pasos de preparación. 
El archivo style.css contiene las reglas de estilo que se aplican a la página web, como el tamaño 
y el tipo de letra, los colores de fondo y los bordes. El archivo add.html es una página web que
permite al usuario agregar nuevas recetas a un libro de cocina. La página tiene un formulario 
que solicita el nombre de la receta, una lista de ingredientes y los pasos de preparación.
Cuando se envía el formulario se genera un pop ap indicando que el dato fue guardado y la nueva 
receta se agrega a la página. Los datos son guardados en formato json mediante locastorage.

Algunas definiciones basicas:

*index.html:
<html>: indica el inicio del documento HTML.
<head>: contiene información sobre el documento, como el título de la página y la referencia al archivo CSS.
<title>: define el título de la página que se muestra en la pestaña del navegador.
<link>: establece la relación entre el documento HTML y el archivo CSS.
<body>: contiene el contenido visible de la página.
<header>: define la sección de encabezado de la página.
<div>: define un contenedor genérico.
<h1>: define un encabezado de nivel 1.
<nav>: define la sección de navegación de la página.
<ul>: define una lista sin ordenar.
<li>: define un elemento de lista.
<a>: define un enlace.
<main>: define la sección principal de la página.
<div>: define un contenedor genérico.
<p>: define un párrafo.
<div>: define un contenedor genérico.
<ul>: define una lista sin ordenar.
<li>: define un elemento de lista.
<div>: define un contenedor genérico.
<h2>: define un encabezado de nivel 2.
<img>: define una imagen.
<ul>: define una lista sin ordenar.
<p>: define un párrafo.

window.onscroll: Esta propiedad se utiliza para detectar cuando el usuario hace scroll en la página. 
Cuando se activa, se llama a la función "scrollFunction()" para realizar una acción específica.

document.body.scrollTop y document.documentElement.scrollTop: Estas propiedades se utilizan para 
obtener la posición actual del scroll en la página. Si la posición es mayor que 20, se muestra un botón 
en la página. Si no, se oculta el botón.

document.getElementById("myBtn").style.display: Esta propiedad se utiliza para mostrar u ocultar el botón 
en la página. Si se establece en "block", el botón se muestra. Si se establece en "none", el botón se oculta.

function topFunction(): Esta función se utiliza para llevar al usuario al inicio de la página cuando 
hace clic en el botón. Establece la posición del scroll en la parte superior de la página.

*add.html:
<form>: define un formulario.
<label>: defineara un elemento de formulario.
<input>: define un campo de entrada de formulario.
<textarea>: define un área de texto de formulario.
<div>: define un contenedor genérico.
<h1>: define un encabezado de nivel 1.
<style>: define las reglas de estilo para la página. 

let recetas = JSON.parse(localStorage.getItem('recetas')) || [];: Esta línea de código carga las recetas 
guardadas en el almacenamiento local del navegador y las almacena en una variable llamada "recetas". 
Si no hay recetas guardadas, se inicializa un arreglo vacío.

function displayrecetas() {...}: Esta función se encarga de mostrar las recetas guardadas en la página web.
Primero, obtiene una referencia al elemento HTML donde se mostrarán las recetas. Luego, borra todo el 
contenido anterior de ese elemento y crea un nuevo elemento HTML para cada receta guardada. Finalmente, 
agrega cada nuevo elemento HTML al elemento principal.

function addreceta(event) {...}: Esta función se encarga de agregar una nueva receta. Primero, obtiene los 
valores de los campos de entrada de la página web. Luego, crea un objeto de receta con esos valores y lo agrega
al arreglo de recetas. Finalmente, guarda el arreglo de recetas actualizado en el almacenamiento local del 
navegador, muestra las recetas actualizadas en la página web y borra los valores de los campos de entrada.

function deletereceta(index) {...}: Esta función se encarga de eliminar una receta existente. 
Toma un índice como argumento, elimina la receta correspondiente del arreglo de recetas y guarda el arreglo 
actualizado en el almacenamiento local del navegador. Luego, muestra las recetas actualizadas en la página web.

document.getElementById('nombre').onchange = function() {...}: Estas líneas de código agregan un controlador de
eventos a cada campo de entrada de la página web. Cuando el usuario cambia el valor de un campo de entrada, el
controlador de eventos elimina cualquier espacio en blanco al principio o al final del valor.

document.getElementById('nombre').onkeyup = function() {...}: Estas líneas de código agregan otro controlador 
de eventos a cada campo de entrada de la página web. Cuando el usuario suelta una tecla mientras escribe en 
un campo de entrada, el controlador de eventos convierte la primera letra del valor en mayúscula.

document.querySelector('form').addEventListener('submit', addreceta): Esta línea de código agrega un 
controlador de eventos al formulario de la página web. Cuando el usuario envía el formulario, el controlador 
de eventos llama a la función "addreceta".

displayrecetas(): Esta línea de código llama a la función "displayrecetas" para mostrar las recetas guardadas 
en la página web cuando se carga la página por primera vez.

function showConfirmation() {...}: Esta función muestra una alerta en la página web cuando se guarda una 
nueva receta.

# actividad-3.1
