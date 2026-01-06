# Cálculo de Paneles

Esta solución calcula cuántos paneles rectangulares pueden colocarse dentro de un techo rectangular utilizando una serie de casos de prueba predefinidos.

## Funcionamiento

El programa recibe las dimensiones del panel y del techo, considerando el ancho y el alto de cada uno.

La lógica utilizada para resolver el problema es la siguiente:

- Los paneles no pueden rotarse.
- Si el panel no cabe físicamente dentro del techo (ya sea en ancho o en alto), el resultado es 0.
- Si el panel cabe dentro de las dimensiones del techo, la cantidad de paneles se calcula dividiendo el área total del techo por el área de un panel, utilizando división entera.

Este enfoque fue elegido por que es simple y coincide con todas la spruevas predefinidas en el json

## Alternativa considerada

Inicialmente pensé una solución basada únicamente en el cálculo del área total del techo y el área de los paneles pero este enfoque no consideraba las dimensiones reales y generaba resultados incorrectos en el último caso de prueba, donde el ancho del panel era mayor que el del techo.

Para resolver este problema, decidí agregar validaciones que verifican que el panel efectivamente quepa dentro del techo antes de realizar el cálculo por área. De esta forma, si el panel es más grande que el techo en cualquiera de sus dimensiones, la función retorna directamente 0, y eso permite manejar todos los casos de prueba

## Cómo ejecutar el programa

Asegurarse de tener Python 3 instalado en el sistema.

Desde la terminal ejecutar este comando: python main.py



