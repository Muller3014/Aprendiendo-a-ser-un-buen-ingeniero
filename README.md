# Aprendiendo a ser un buen ingeniero - Gonzalo Müller

https://github.com/Muller3014/Aprendiendo-a-ser-un-buen-ingeniero.git

El caballo tiene distintas opciones de movimiento en función de su posición. Puede tener cero, dos o tres movimientos posibles. A continuación se detalla la situación para cada número del tablero:

Desde 0, puede moverse a 4 o 6 (2 opciones).
Desde 1, puede ir a 6 o 8 (2 opciones).
Desde 2, las opciones son 7 o 9 (2 opciones).
Desde 3, puede ir a 4 o 8 (2 opciones).
Desde 4, puede desplazarse a 3, 9 o 0 (3 opciones).
Desde 5, no tiene movimientos posibles (0 opciones).
Desde 6, puede moverse a 1, 7 o 0 (3 opciones).
Desde 7, las opciones son 2 o 6 (2 opciones).
Desde 8, puede ir a 1 o 3 (2 opciones).
Desde 9, puede ir a 2 o 4 (2 opciones).

Así, podemos organizar las posibilidades de la siguiente forma:

C(0) = (4, 6)
C(1) = (6, 8)
C(2) = (7, 9)
C(3) = (4, 8)
C(4) = (3, 9, 0)
C(5) = ()
C(6) = (1, 7, 0)
C(7) = (2, 6)
C(8) = (1, 3)
C(9) = (2, 4)

Si sumamos todas estas opciones, obtenemos un total de 20 movimientos posibles para un solo movimiento: 

<code>2+2+2+3+0+3+2+2+2+2=20</code> , que se ajusta a lo indicado en el enunciado.

Ahora, para determinar las opciones con dos movimientos, definimos un conjunto de posibilidades (M), que incluye la posición inicial (n) y los movimientos restantes (N). Por ejemplo, para el número 4:

<code>M(4,2)=M(3,1)+M(9,1)+M(0,1)=2+2+2=6</code> posibilidades.


Haciendo lo mismo para el 9:

<code>M(9,2)=M(2,1)+M(4,1)=2+3=5</code> posibilidades.

Este cálculo se realiza para los otros números, resultando en un total de 46 posibilidades para dos movimientos, alineándose con los datos proporcionados.

Siguiendo este mismo razonamiento, la fórmula para calcular los caminos posibles se puede expresar de una manera general. A partir de aquí, se pueden determinar las posibilidades solicitadas en el problema:

- Para 1 movimiento: 20 posibilidades.

- Para 2 movimientos: 46 posibilidades.

- Para 3 movimientos: 104 posibilidades.

- Para 5 movimientos: 544 posibilidades.

- Para 8 movimientos: 6576 posibilidades.

- Para 10 movimientos: 34432 posibilidades.

- Para 15 movimientos: 2140672 posibilidades.

- Para 18 movimientos: 25881088 posibilidades.

- Para 21 movimientos: 307302400 posibilidades.

- Para 23 movimientos: 1609056256 posibilidades.

- Para 32 movimientos: 2792668987392 posibilidades.

