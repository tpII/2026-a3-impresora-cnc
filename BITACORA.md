Bitácora de Desarrollo — A3 Plotter CNC
Materia: Taller de Proyecto II
Integrantes: Graziani Martín, Reyes Manuel y Rodríguez Joaquín



Semana del 6/9

* Elección del proyecto plotter CNC
* Análisis general del proyecto
* Preparacion del primer informe
* Escritura del plan de proyecto
* Diseño de la presentación
* Video de la presentación
* Primer boceto de interfaz
* Relevamiento de requerimientos



Semana del 13/09

* Primer entrega





Semana del 22/09

* Solicitud de materiales principales y secundarios





Semana del 28/9

* Entrega de materiales
* Compra de componentes eléctricos
* Preparacion y terminacion de la estructura 3d
* Ensamblaje
* Primeras pruebas individuales
* Preparación del informe de avance







Semana del 5/10

* Entrega de materiales faltantes



Semana del 11/10

* Segunda entrega

Semana 19/10 
Análisis del código de GRBL de instructables: analizamos el codigo GRBL para el control del plotter

Descarte de GRBL de instructables: Determinamos que no nos servía porque está diseñado específicamente para la arquitectura AVR de Arduino. Al utilizar un ESP32, tendríamos que modificar prácticamente todo el código base.

Investigación de alternativas: Buscamos bibliotecas compatibles con el esp.

Selección de biblioteca: Optamos por la librería ESP GRBL, que está orientada a impresoras 3D y podemos reciclar funciones para el proyecto y ademas esta diseñada ya para el ESP32 sin cambiar nada https://github.com/bdring/Grbl_Esp32.

Esta semana

Implementación de la nueva librería: Comenzamos a trabajar con ESP GRBL como base.

Integración del sistema: Primer boceto del codigo ya funcional, integramos la interfaz que teniamos con la biblioteca y fuimos probando con Claude hasta llegar a que ya dibuje la imagen.

Primera prueba funcional de trazado: Llegamos a un programa que dibuja algo bastante similar a la imagen ingresada, usando figuras muy simples.

Probamos dos alternativas para adaptar las dimensiones: hacer que el programa achique la imagen vs. limitar el tamaño máximo de la imagen que puede ingresar el usuario.

Por ahora elegimos limitar el tamaño de entrada porque sino se tenia que achicar demasiado la imagen, se rompia mucho y nos parecio mejor limitar el tamaño de la imagen ingresada , así se adapta mejor con límites físicos del plotter.

Identificación de pendientes y optimizaciones:

Falta ajustar algunas cosas y calibrar porque todavía tiene poca precisión, necesitamos empezar a modificar el código para ir optimizándolo.

