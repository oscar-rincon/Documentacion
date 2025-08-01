---
title: Integración FEM parte 1 - Imágenes como datos de entrada 
tags: Acta
---
**Grupo Miércoles**

## Problema
A partir de los datos de entrada que se van a generar, los cuales se decidieron que serán imágenes binarias de 64x64, se plantea realizar la lectura de datos y su asignación como material del elemento para cada elemento generado en el modelo de elementos finitos.

## Desarrollo de la reunión
- Se definió que la primera tarea es la generación de la geometría del problema 2D. Esta geometría será cuadrada, con una longitud constante $a$ para cada uno de los modelos generados. La resolución de los elementos cuadrados que conforman la malla de FEM será equivalente por la resolución de la imagen de entrada. Para aclarar esto último, se presenta el siguiente ejemplo: Si se cuenta con una imagen de entrada de 64x64 bits, entonces el tamaño del elemento de FEM se define como $a/64$, pero si en un futuro se desea ingresar una imagen con resolución de 512x512 bits, el tamaño del elemento ahora debe ser de $a/512$.

Esta tarea se piensa realizar a partir de herramientas de generación de geometrías como GMSH o funciones internas de SolidSpy para la generación de geometrías y mallas cuadradas.

- Una vez completada la primera tarea, se debe desarrollar una rutina que permita asignar a cada elemento de la malla uno de dos materiales posibles, siguiendo el orden de asignación establecido por la imagen de entrada.

<p align="center">
    <img src="{{ site.baseurl }}/assets/img/integracionFEMdiagrama.png" alt="Diagrama de creación de geometría y asignación de material en FEM" width="800">
</p>

## Compromisos Futuros
- Escribir las rutinas que permiten completar las tareas estabelecidas en la reunión.
- Resolver la pregunta, ¿Qué condiciones de frontera se deben imponer al problema FEM para poder solucionarlo?
