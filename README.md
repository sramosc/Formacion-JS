Curso JS
--------

Andrea Puddu 
tw: @nuragic 
url: www.nuragic.io

Objetivos
---------

Crear una app desde el principio

* Carga de dependencias: script, async, defer, "module", "module" async
* strict mode: modulos y clases siempre son estrictos
* Recomendable el uso de ESLint

VARIABLES
---------

* VAR, LET Y CONST:
* Razones de no usar var:
  * Puede crear variables globales
  * No tiene ámbito de bloque (hoisting + ambito de funcion)
  * A partir de ES6 usar let y const

* let:
  * Tiene ambito de bloque, no aplica hoisting
  * No permite redeclarar

* const:
  * Igual que LET
  * Debe ser inicializada
  * Su valor no puede ser reasignado, salvo que sea un Object o un Array, mediante los metodos propios de añadir datos (shift,push,...)

DESTRUCTURING
-------------

  1.- Permite acceder a todos o varios de los valores de un objeto de golpe
  2.- Asignacion multiple:
      const o = { a:1, b:2}
      const {a:first,b:second} = o;
  3.- Asignacion parcial:
      > var [x,y] = [3];
      > x
      < 3
      > y
      < undefined
  4.- Uso de funciones implicitas en la asignacion
      > var (length : len) = 'abc';
      > leng
      < 3
  5.- Asignaciones que se saltan un valor:
      > var [a, ,b]=[0,1,2]
      > a
      < 0
      > b
      < 2
  6.- Asignaciones reciprocas:
      > [a,b]=[b,a]

OBJECTS
-------

  * Uso del Object.assign:
    > var oo = Object.assign({a:1},{b:{c:1,d:3}});
    < undefined
    > oo
    < {a: 1, b: {…}}
  * Uso de .__proto__:
    - En desuso, obsoleto. No se debería usar.
    - Object.getPrototypeOf(Object); devuelve el mismo resultado
    - Uso de expresiones dinamicas para creacion de propiedades:
      > var prefix = '__';
      > var ooo = { [prefix] + 'Foo': 'bar'};
    - Uso de shorthands para reducir código (en getters y setters)

SPREAD / GENERADORES
--------------------

  * Uso del ... para obtener de golpe el contenido de un array como valores individuales
  * Potencia la extraccion de datos

ARROW FUNCTIONS
---------------

  * (parametros opcionales) => {cuerpo de la funcion}

EXPRESIONES REGULARES, CODIFICACION, ETC.
-----------------------------------------

  * template literal: ${identificador}
