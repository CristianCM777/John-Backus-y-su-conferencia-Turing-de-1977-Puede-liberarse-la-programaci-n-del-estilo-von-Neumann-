# John Backus Conferencia Turing de 1977

-Alumno: Camarillo Molina Cristian 23210553

-Maestro: Rene Solis Reyes 

-Materia: Programación lógica y funcional 

-Horario: 4 - 5pm

## Introduccion
John Backus es reconocido por haber liderado el desarrollo de FORTRAN y la notacion BNF, dos pilares del diseño de lenguajes de programacion. Sin embargo, en su discurso del premio Turing de 1977 planteo la critica contundente contra el paradigma que el mismo ayudo a consolidar. Su argumento central fue que la mayoria de los lenguajes de programacion (Como FORTRAN, ALGOL o Pascal) estan atados a la arquitectura fisica de von Neumann. Esta dependencia obliga a los programadores a pensar en términos de modificación de memoria palabra por palabra, impidiendo que el software tenga propiedades algebraicas claras.

## Desarrollo 
El problema principal que señala Backus no es solo la limitación del bus físico entre la CPU y la memoria (el cuello de botella de von Neumann), sino la impronta que este deja en la sintaxis de los lenguajes. Las sentencias de asignación ($x := e$) y los bucles iterativos son reflejos directos del movimiento de datos en el hardware.

Para solucionar esto, Backus propuso el Sistema FP (Functional Programming), el cual se distingue por ser completamente libre de variables (point-free):

- Objetos: Atomos o secuencias(<1,2,3>)
- Funciones primitivas: Operaciones puras que no modifican su estado(+, x, trans).
- Formas combinatorias: Operadores de orden superior que combinan funciones sin nombrar sus argumentos (f o g, [f1, f2], alpha(f), /f). s

