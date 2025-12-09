# **PRUEBA INDIVIDUAL – RA2 - HTML+CSS AIDAN GUZMÁN POSTIGO**

## Ejercicio 1

### Ejercicio 1A
No se centra porque (además de que falta enlazar el css en el archivo html) el header de la web se está mostrando con flex sin utilizar una flex direction así que se mantiene centrado respecto al eje x (vertical), se puede cambiar poniendo un flex direction column para que se centre respecto al eje y (horizontalmente).

### Ejercicio 1B
Para centrarlo usando flex es tan sencillo como usar flex direction column para que se distribuya en columnas y luego usar align items: center para que se centre respecto al eje y.

```css
.site-header {
  display: flex;
  align-items: center;
  flex-direction: column;
}
```
Para centrarlo usando grid podemos usar la propiedad justify-items además de utilizar display: grid para que se centre respecto al eje y.
```css
.site-header {
  display: grid;
  justify-items: center;
}
```
### Ejercicio 1C
Voy a usar la misma estructura con flex del ejercicio anterior añadiendo un gap que sirve para dar margen entre los elementos del header.
```css
.site-header {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 30px;
}
```
### Ejercicio 1D
Teniendo de base lo realizado en el anterior ejercicio, le aplicamos background-color para aplicar un color al fondo del header, luego un border-bottom para aplicar un borde inferior, en este caso usando el estilo dotted, con un tamaño de 5px y de color verde, luego usar un box-shadow para aplicar más separación visual entre el header, el resto de los elementos y por último he aplicado padding para que los elementos de dentro del header no se queden pegados a los bordes.
```css
.site-header {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 30px;
  background-color: aquamarine;
  border-bottom: dotted green 5px;
  box-shadow: 10px 10px 5px 0px rgba(0,0,0,0.75);
  padding: 1em;
}
```
## Ejercicio 2

### Ejercicio 2A
Simplemente cambio el <button> para introducirlo al header, de manera que queda así:
```html
<header class="site-header">
    <h1>Balatro</h1>
    <nav class="main-nav">
      <ul>
        <li><a href="#hero">Inicio</a></li>
        <li><a href="#galery">Galería</a></li>
        <li><a href="#table">Manos</a></li>
        <li><a href="#form">Suscripción</a></li>
        <li><a href="#RRSS">Contacto</a></li>
      </ul>
    </nav>
    <button class="open-menu" aria-label="Abrir menú lateral"><img id="toggleIcon" src="img/ficha_menu_notOpen.png" alt="Icono del menú"></button>
  </header>
```
### Ejercicio 2B
Primero para poder maquetar el header utilizamos flex alineando los objetos a la derecha con justify-content:rigth haciendo que todos elementos se muevan hacia el borde horizontal derecho, luego en el h1 colocamos la propiedad position absolute para que de manera inmutable el elemento (en este caso el h1) se quede en la posición que se quiera, en este caso utilizando left: 50% forzamos a que el titulo se quede centrado horizontalmente, respecto al botón utilizamos position: fixed para que siempre se quede en la misma posición, incluso si abrimos la página en dispositivos con una pantalla más pequeña.
```css
.site-header {
  position: sticky;
  top: 0;
  z-index: 10;
  background-color: #1b5349;
  padding: 1em;
  display: flex;
  align-items: center;
  justify-content: right;
}
.site-header h1 {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  font-family: "Balatro";
}
.site-header a {
  font-family: "Balatro";
}
.main-nav ul {
  list-style: none;
  display: flex;
  gap: 10px;
}
.open-menu {
  position: fixed;
  top: 14px;
  left: 10px;
  z-index: 20;
  font-size: 26px;
  background: none;
  border: none;
  cursor: pointer;
  transition: transform 0.3s ease, background-color 0.3s ease;
  font-family: "Balatro";
}
.side-menu {
  position: fixed;
  top: 0;
  left: -230px;            
  width: 230px;
  height: 100%;
  padding-top: 60px;
  transition: left 0.3s ease;
  z-index: 15;
  background-color: #11685b;
  font-family: "Balatro";
}
.side-menu.active {
  left: 0;                 
}
```
## Ejercicio 3

### Ejercicio 3A
En este caso ya tenía las imágenes como miniaturas ya que al haber usado grid y varias imágenes por fila se hicieron más pequeñas además de aplicarles un 80% de width para que se viesen aún más pequeñas.

### Ejercicio 3B
En este caso ya disponía de un efecto para cuando el ratón pasase por las imágenes, justamente "transform: scale(1.03);" que está aplicado a todas las imágenes de la página web que contienen cualquier tipo de enlace, respecto al borde se le ha añadido un borde con background-color a todas las imágenes cuando el cursor pasa por ellas.

### Ejercicio 3C
Mi página web también contaba con esta característica que simplemente es añadir un enlace a la imágen para que lleve a la ruta donde la imagen completa está alojada.

Resultado final: 
```html
<section id="galery">
      <h2>Galería de imágenes</h2>
      <figure>
        <a href="img/gallery1.png"><img src="img/gallery1.png" alt="Imagen galería 1"></a>
        <a href="img/gallery2.png"><img src="img/gallery2.png" alt="Imagen galería 2"></a>
        <a href="img/gallery3.png"><img src="img/gallery3.png" alt="Imagen galería 3"></a>
        <a href="img/gallery4.png"><img src="img/gallery4.png" alt="Imagen galería 4"></a>
        <a href="img/gallery5.png"><img src="img/gallery5.png" alt="Imagen galería 5"></a>
        <a href="img/gallery6.png"><img src="img/gallery6.png" alt="Imagen galería 6"></a>
        <a href="img/gallery7.png"><img src="img/gallery7.png" alt="Imagen galería 7"></a>
        <a href="img/gallery8.png"><img src="img/gallery8.png" alt="Imagen galería 8"></a>
        <a href="img/gallery9.png"><img src="img/gallery9.png" alt="Imagen galería 9"></a>
        <a href="img/gallery10.png"><img src="img/gallery10.png" alt="Imagen galería 10"></a>
        <a href="img/gallery11.png"><img src="img/gallery11.png" alt="Imagen galería 11"></a>
        <a href="img/gallery12.png"><img src="img/gallery12.png" alt="Imagen galería 12"></a>
      </figure>
    </section>
```
```css
a:hover{
  background-color: #1b3748;
}
main a{
  text-decoration: underline #1b3748;
}
#galery figure {
  display: grid;
  grid-template-rows: repeat(3, auto);
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
}

#galery img {
  width: 80%;
  height: auto;
  object-fit: cover;
  border-radius: 10px;
  margin: auto;
  display: block;
}
```
## Ejercicio 4

### Ejercicio 4.1
Mi página web trata sobre Balatro, un juego roguelike que a nivel personal me ha inspirado bastante, en la web he incluido varios articulos con información sobre el juego como  el contenido mecánico de este, información sobre el autor, la importancia de este juego en la industria y la explicación mecánica del juego, además de esto he incluido secciones como la galería, un formulario, una tabla con las manos del juego y una lista con las redes oficiales tanto del juego como del creador, la idea de diseño es que fuese atractivo a la vista y que generase interés en el lector para probar el juego, la paleta de colores está inspirada en el juego.

### Ejercicio 4.2
