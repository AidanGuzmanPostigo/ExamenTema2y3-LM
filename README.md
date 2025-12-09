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
```
.site-header {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 30px;
}
```
### Ejercicio 1D
Teniendo de base lo realizado en el anterior ejercicio, le aplicamos background-color para aplicar un color al fondo del header, luego un border-bottom para aplicar un borde inferior, en este caso usando el estilo dotted, con un tamaño de 5px y de color verde, luego usar un box-shadow para aplicar más separación visual entre el header, el resto de los elementos y por último he aplicado padding para que los elementos de dentro del header no se queden pegados a los bordes.
```
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
