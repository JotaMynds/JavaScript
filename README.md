# JAVASCRIPT
## INTRODUCCIÓN AL TEMARIO

JavaScript es un lenguaje de programación de scripts (secuencia de comandos) orientado a objetos.
Es un lenguaje interpretado por el navegador, que nos permite crear páginas dinámicas en las que el usuario puede interacturar fácilmente

## FORMAS DE USO

1. Embeber el codigo en el documento HTML con la etiqueta <script></script>.
2. Mediante archivos externos para ayudar a la coherencia y a la organización.
3. A través de elementos HTML con referencias de funcionalidades JavaScript.

## HOLA MUNDO

La consola de JavaScript se utiliza normalmente para la depuración de nuestro código. De esta manera podemos
enviar el valor de alguna variable, o el resultado esperado de una función para comprobar si el código está haciendo
lo que se esperaba.

**console.log("Hola mundo :D");**

Si queremos borrar el contenido de la consola podemos utilizar la sentencia console.clear() o el atajo de teclado
CRTL+L.

## OPERADOR DE ASIGNACIÓN

Una asignación consta de 2 partes:
- a la izquierda una variable
- a la derecha el valor asignado

Se utiliza 'var' para declarar variables pero también se utiliza 'let'

### EJEMPLO

Código 1: asignaciones

var x;
var y = 6;
x = 5
var z = x + y;

## TIPOS DE DATOS

• Null: Define objetos que aún no existen.
• Numéricas: Almacenan valores numéricos enteros o decimales.
• Cadenas de texto: Permiten almacenar literales.
• Arrays: Permite almacenar una colección de valores.
• Booleanos: Puede tomar el valor true o false.
• Objetos: Contiene colección de propiedades

### EJEMPLO

Código 2: Distintos tipos de datos

var temp = 16 + "Gato";

Se declara una variable temp y se le asigna el valor 16 y << Gato >>.
En este caso se podría dudar del resultado puesto que 16 es un valor entero y << Gato >> es una cadena de caracteres
La forma en la que JavaScript interpreta esto es <<16Gato>>.

### CALCULOS BASICOS QUE PODEMOS HACER

var resultado = 3+2;
alert(resultado);
(muestra 5)

var resultado = 3-2;
alert(resultado);
(muestra 1)

var resultado = 6/2;
alert(resultado);
(muestra 3)

var num1 = 3, num2= 2, resultado
resultado = num1 * num2;
alert(resultado);
(muestra 6)

var numero = 3;
numero += 5;
(muestra 8)

### CONCATENACIÓN DE DATOS

var texto = "hola";
texto += "Tu"
alert(texto);
(salida: hola Tu)

PARA INTERACTUAR CON EL USUARIO USAMOS "PROMP()"

var NombreUsuario = Promp('Introduce el nombre:');
alert(NombreUsuario);

TAMBIEN PODREMOS USAR document.write(''); PARA INCLUIR INFORMACIÓN EN EL DOCUMENTO

### CONVERSIONES 

código 4: Error de conversión

var age = Number("Valor textual");
alert(age); //NaN, conversion

### Ejemplo

Código 5. Conversión de números, cadena y boolean

alert(Boolean(1)); //true
alert(Boolean(0)); //false
alert(Boolean("Hola")); //true
alert(Boolean()); //false

### OPERADORES ARITMÉTRICOS Y COMPARADORES

Los operadores nos van a permitir realizar diferentes operaciones con las variables. Los principales operadores son:

• Asignación (=): Permite guardar un valor en la variable.
• Incremento(++) y decremento(--): Para valores numéricos y permiten incrementar o decrementar su valor.
• Operador de negación (!): Obtiene el valor contrario del valor de la variable. Se usa con variables boolenas.
• Operador AND(&&): Combina dos variables boolenas. Se obtiene valor verdadero si ambas son verdaderas.
• Operador OR(||): Combina dos variables boolenas. Se obtiene valor verdadero si alguna es verdadera.
• Operador suma(+), resta(-), multiplicación(*) y división(/).
• Operadores mayor que (>), menor que (<), mayor o igual (>=), menor o igual (<=), igual que (==) y distinto
de (!=). Compara dos valores y devuelve true o false dependiendo de la comprobación.

## SENTENCIAS

### BLOQUES DE CODIGO

Código 8: Bloque de código con nombre

function test(){
    var a, b, c;
    a = 5;
    b = 6;
    c = a+b;
}

### SENTENCIA IF-ELSE

Código 6: Sentencia If-else

var result;
if (a > 0) {
result = "positive";
  } else {
    result = "NOT positive";
  }
return result;

### SENTENCIA SWITCH

Código 7: Sentencia Switch

var foo = 1;
var output = "Salida: ";

switch (foo) {

  case 10:
    output += "¿Y ";

  case 1:
    output += "Cuál ";
    output += "Es ";

  case 2:
    output += "Tu ";

  case 3:
    output += "Nombre";

  case 4:
    output += "?";
    console.log(output);
    break;

  case 5:
    output += "!";
    console.log(output);
    break;

  default:
    console.log("Por favor, selecciona un valor del 1 al 6.");
}

De forma estandar se suele poner 'break;' en cada caso del switch.

### SENTENCIA FOR

Código 8: Bucle For

for (var i = 0; i < 9; i++) {
  n += i;
  console.log(n);
}


### SENTENCIA WHILE

Código 9: Bucle While

n = 0;
x = 0;

while (n < 3) {
  n++;
  x += n;
}

### COMENTARIOS

Comentario de línea se utiliza con //
Comentario de párrafo se utiliza /* mensaje */

# DOCUMENT OBJECT MODEL (DOM)

En JavaScript, la forma de acceder al DOM es a través de un objeto llamado document, que representa el árbol DOM de la página o pestaña donde nos encontramos.

## TIPOS DE NODOS

En total existen 12 tipos de nodos, pero los más utilizados y los que vamos a ver son:

• document: Nodo raíz.
• element: Etiquetas HTML.
• attr: Atributos de las etiquetas HTML.
• text: Contenido de las etiquetas HTML.
• comment: Comentarios de la página HTML

## SELECCIONAR ELEMENTOS DOM

Solemos identificar generalmente através del id o la clase
Para ello tenemos el método .getElementById("id") que busca un elemento HTML con el id especificado.

## ACCESO A NODOS

• getElementsByTagName(etiqueta): Obtiene todos los elementos del documento HTML cuyas etiquetas
coincidan con la etiqueta pasada por parámetro. Devuelve un array con los elementos que coincidan.

• getElementsByName(nombre): Obtiene los elementos cuyo atributo name es igual al pasado por parámetro.
Devuelve un array.

• getElementById(identificador): Obtiene el elemento HTML cuyo identificador coincide con el pasado por
parámetro. Devuelve un elemento.

• getElementsByClassName(clase): Obtiene los elementos cuya clase coincide con la pasada por parámetro.
Devuelve un array.

## CREAR ELEMENTOS 

Código 10: Crear con el método .createElement()

var elemento = document.createElement("Nombre de la etiqueta");

Código 11: Crear nodo con el método

Código 12: agregar un nuevo método

# INFORMACIÓN ADICIONAL 
## FUNCIONES Y PROPIEDADES PREDEFINIDAS
### MANEJO DE CADENAS DE TEXTO

Manejo de cadenas de texto:

• length: Propiedad que indica la longitud del literal.

• concat(literal): Función que permite concatenar literales.

• toUpperCase(literal): Función que transforma los caracteres en mayúsculas.

• toLowerCase(literal): Función que transforma los caracteres en minúsculas.

• charAt(posicion): Función que devuelve el carácter que ocupa la posición indicada en una cadena de
texto.

• indexOf(caracter): Función que devuelve dónde se encuentra el carácter indicado dentro de un literal.

• substring(inicio,final): Extrae un trozo de la cadena de texto que comience en inicio y termina en final.

• split(separator): Función que separa una cadena de texto en un array de cadenas de texto, que se
encuentran separados por el separador indicado.

### MANEJO DE ARRAYS

• length: Propiedad que da el número elementos del array.

• join(separator): Convierte los elementos de un array en una cadena de texto utilizando separator como
separador.

• pop(): Elimina el último elemento del array.

• push(): Función que añade un elemento al final del array.

• shift(): Elimina el primer elemento del array.

• unshift(): Añade un elemento al principio del array.

• reverse(): Coloca los elementos del array en orden inverso.

## BIBLIOGRAFÍA

[text](https://developer.mozilla.org/es/docs/Web/JavaScript)
