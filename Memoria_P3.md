<div align="center"><img src="logo.png"  width="300" height="200">

</br>

# **MEMORIA PRÁCTICA 3 - INTELIGENCIA ARTIFICIAL**
## Búsqueda con Adversario (Juegos)
### El Parchís (con un twist) </div>

> **Alumno**: Quintín Mesa Romero

>  **Curso**: 3º DGIIM
  
>  **DNI**: 78006011Q
  
>  **Correo**: quintinmr@correo.ugr.es

</br>
</br>

## Introducción

En el presente documento se ha elaborado un análisis del problema que se aborda en la práctica en el que se ha especificado cuál es el objetivo del mismo y se ha especificado, sin entrar demasiado en detalle, cómo se ha abordado. A continuación, se ha descrito, ahora sí con más detalle, la solución que se ha planteado para resolver el problema.

## Análisis del Problema

En esta práctica se nos pide desarrollar un programa que implemente un algoritmo MINMAX o Poda Alpha-Beta con objeto de derrotar a 3 Ninjas jugando al famoso juego del parchís. Además, se nos pide definir una heuristica adecuada que, al incorporarla al algoritmo de Poda que hemos implementado, logremos haber creado un buen jugador inteligente de parchís.

Para la elaboración del algoritmo de poda alpha-beta, he seguido las directrices establecidas por la profesora durante la resolución de problemas de esta índole.

La heurística que he definido para la práctica otorga un valor a los nodos hoja del árbol con base a cómo de bueno es para el jugador que nos representa el estado de las fichas en el tablero.

## Descripción de la solución planteada

**Algoritmo Poda Alpha-Beta**: el algoritmo que se ha implementado nos devuelve, a parte de la valoración minmax del juego, gracias a los pasos por referencia de los parámetros, la siguiente acción a realizar por el jugador: la ficha que tenemos que mover, y cómo. Destaco que los nodos hijos se han ido generando de mayor a menor; se ha ido generando el siguiente movimiento siguiendo un orden descendente de los dados. Es por ello que se ha empleado la función de la clase Parchis, *generateNextMoveDescending(colorPieza, dado, idDado)*.

**Heurística empleada**: 

* *Heurística 1*: Lo primero que se nos podría ocurrir para hacer nuestro jugador un poco más inteligente es que tuviera en cuenta a la hora de elegir la siguiente acción, la distancia de las fichas del jugador a su meta.Así, he definido una primera heurística que logra ganar al ninja 1, pero nada más.

* *Heurística 2*: Luego, si pensamos en cómo elegir de la forma más adecuada posible la siguiente ficha a mover, se nos vienen a la cabeza varias cosas a tener en cuenta que otorgarán mayor valor a una casilla que a otra: 
    
    * La distancia de las fichas a la meta se ha de tener en cuenta: cuanto más cerca estén de la meta, más valor tiene esa ficha frente a otra que esté más lejos.

    * Si tenemos fichas en la casa, las fichas que estén en terreno de juego corren más peligro, por tanto, se da menos valor a las que estén en casa. De la misma forma, las fichas que estén en zona segura, tendrá más valor que otras.

    * El número de fichas que tengamos en la meta frente a las que tenga el adversario.





