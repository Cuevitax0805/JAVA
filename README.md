# JAVA
Variables y Estructuras
# JAVA — VARIABLES Y ESTRUCTURAS

Repositorio de recopilación, documentación y aprendizaje de los fundamentos del lenguaje de programación Java.

Este repositorio contiene una guía de referencia sobre la sintaxis, variables, tipos de datos, operadores, estructuras de control, métodos, arreglos, colecciones y programación orientada a objetos.

---

## 📑 ÍNDICE

1. [Introducción a Java](#1-introducción-a-java)
2. [Estructura básica de un programa](#2-estructura-básica-de-un-programa)
3. [Variables y constantes](#3-variables-y-constantes)
4. [Tipos de datos](#4-tipos-de-datos)
5. [Conversión de tipos](#5-conversión-de-tipos)
6. [Operadores](#6-operadores)
7. [Entrada y salida de datos](#7-entrada-y-salida-de-datos)
8. [Estructuras condicionales](#8-estructuras-condicionales)
9. [Estructuras repetitivas](#9-estructuras-repetitivas)
10. [Arreglos](#10-arreglos)
11. [Cadenas de caracteres](#11-cadenas-de-caracteres)
12. [Métodos y funciones](#12-métodos-y-funciones)
13. [Programación orientada a objetos](#13-programación-orientada-a-objetos)
14. [Modificadores de acceso](#14-modificadores-de-acceso)
15. [Herencia y polimorfismo](#15-herencia-y-polimorfismo)
16. [Interfaces y clases abstractas](#16-interfaces-y-clases-abstractas)
17. [Colecciones](#17-colecciones)
18. [Manejo de excepciones](#18-manejo-de-excepciones)
19. [Operaciones con archivos](#19-operaciones-con-archivos)
20. [Paquetes e importaciones](#20-paquetes-e-importaciones)
21. [Expresiones lambda](#21-expresiones-lambda)
22. [Buenas prácticas](#22-buenas-prácticas)
23. [Estructura de un proyecto Java](#23-estructura-de-un-proyecto-java)

---

## 1. INTRODUCCIÓN A JAVA

Java es un lenguaje de programación de propósito general, orientado a objetos y diseñado para desarrollar aplicaciones en diferentes plataformas.

Su funcionamiento se basa en la compilación del código fuente a bytecode, que posteriormente es ejecutado por la Java Virtual Machine (JVM).

### Características principales

- Es un lenguaje orientado a objetos.
- Es multiplataforma mediante la JVM.
- Posee un sistema de tipos estático.
- Dispone de gestión automática de memoria mediante el recolector de basura (Garbage Collector).
- Permite desarrollar aplicaciones de escritorio, web, empresariales y móviles.
- Cuenta con una amplia biblioteca estándar.
- Soporta concurrencia y programación multihilo.

### Conceptos fundamentales

| Concepto | Descripción |
|---|---|
| JDK | Kit de desarrollo que incluye herramientas para desarrollar aplicaciones Java. |
| JRE | Entorno de ejecución de Java. |
| JVM | Máquina virtual encargada de ejecutar el bytecode. |
| JIT | Compilador que optimiza partes del código durante la ejecución. |
| Bytecode | Código intermedio generado al compilar un programa Java. |

---

## 2. ESTRUCTURA BÁSICA DE UN PROGRAMA

Un programa Java se organiza mediante clases y métodos.

### Ejemplo:

```java
public class Main {

    public static void main(String[] args) {

        System.out.println("Hola, mundo");

    }

}
```

### Explicación

- `public`: modificador de acceso.
- `class`: palabra reservada para declarar una clase.
- `Main`: nombre de la clase.
- `static`: permite ejecutar el método sin crear una instancia de la clase.
- `void`: indica que el método no devuelve ningún valor.
- `main`: método de entrada tradicional del programa.
- `String[] args`: recibe argumentos enviados al programa.
- `System.out.println()`: imprime información y añade un salto de línea.

### Comentarios en Java

Los comentarios permiten documentar el código sin que formen parte de las instrucciones ejecutadas.

**Comentario de una línea:**

```java
// Este es un comentario de una línea
```

**Comentario de varias líneas:**

```java
/*
Este es un comentario
de varias líneas.
*/
```

**Comentario de documentación:**

```java
/**
 * Método principal del programa.
 */
```

Los comentarios de documentación pueden utilizarse para generar documentación mediante Javadoc.

---

## 3. VARIABLES Y CONSTANTES

Las variables son espacios de memoria identificados mediante un nombre y utilizados para almacenar información durante la ejecución del programa.

En Java, cada variable tiene un tipo de dato definido.

### Declaración de variables

```java
int edad;

edad = 20;
```

También es posible declarar e inicializar una variable en una sola instrucción:

```java
int edad = 20;
```

### Sintaxis general

```java
tipo nombreVariable = valor;
```

### Ejemplos:

```java
String nombre = "Juan";

int edad = 20;

double altura = 1.80;

boolean estudiante = true;

char inicial = 'J';
```

### Reglas para nombrar variables

- Deben comenzar con una letra, guion bajo (`_`) o símbolo de dólar (`$`).
- No pueden comenzar con un número.
- No pueden utilizar palabras reservadas.
- Java diferencia entre mayúsculas y minúsculas.
- Se recomienda utilizar `camelCase` para los nombres de variables.

Ejemplo:

```java
String nombreCompleto = "Juan Cuevas";

int numeroDeUsuarios = 100;
```

### Constantes

Las constantes son variables cuyo valor no puede modificarse después de su inicialización.

Para declararlas se utiliza la palabra reservada `final`.

```java
final double PI = 3.14159;

final int EDAD_MINIMA = 18;
```

Por convención, los nombres de las constantes se escriben en mayúsculas y separando las palabras con guiones bajos.

---

## 4. TIPOS DE DATOS

Java dispone de dos grandes categorías de tipos de datos: primitivos y de referencia.

### Tipos de datos primitivos

Son los tipos básicos incorporados en el lenguaje.

| Tipo | Tamaño | Descripción | Ejemplo |
|---|---:|---|---|
| `byte` | 8 bits | Entero pequeño. | `byte numero = 10;` |
| `short` | 16 bits | Entero corto. | `short numero = 1000;` |
| `int` | 32 bits | Entero estándar. | `int edad = 20;` |
| `long` | 64 bits | Entero largo. | `long poblacion = 8000000L;` |
| `float` | 32 bits | Número decimal de precisión simple. | `float precio = 10.5f;` |
| `double` | 64 bits | Número decimal de doble precisión. | `double altura = 1.80;` |
| `char` | 16 bits | Unidad de código UTF-16. | `char letra = 'A';` |
| `boolean` | No especificado por el lenguaje | Valor verdadero o falso. | `boolean activo = true;` |

### Tipos de referencia

Almacenan referencias a objetos y permiten trabajar con estructuras más complejas.

| Tipo | Descripción | Ejemplo |
|---|---|---|
| `String` | Cadena de caracteres. | `String nombre = "Juan";` |
| Arrays | Conjunto de elementos del mismo tipo. | `int[] numeros = {1, 2, 3};` |
| Clases | Permiten crear objetos. | `Persona persona = new Persona();` |
| Interfaces | Definen contratos de comportamiento. | `Runnable tarea;` |
| Enums | Representan conjuntos de constantes. | `Color color = Color.ROJO;` |

### Diferencia entre tipos primitivos y de referencia

- Los tipos primitivos almacenan directamente valores.
- Los tipos de referencia contienen referencias a objetos.
- Los tipos primitivos no pueden tener el valor `null`.
- Las variables de referencia pueden tener el valor `null`.

---

## 5. CONVERSIÓN DE TIPOS

La conversión de tipos permite transformar un valor de un tipo de dato a otro.

En Java existen dos formas principales.

### Conversión implícita (Widening)

Se produce automáticamente cuando se convierte un tipo de menor capacidad a otro compatible de mayor capacidad.

```java
int numero = 100;

double resultado = numero;

System.out.println(resultado);
```

### Conversión explícita (Casting)

Se utiliza cuando se transforma un tipo de mayor capacidad a otro de menor capacidad.

```java
double precio = 19.99;

int precioEntero = (int) precio;

System.out.println(precioEntero);
```

Resultado:

```text
19
```

En este caso, se pierde la parte decimal.

### Conversión de cadenas

Para convertir texto a números se pueden utilizar métodos de las clases envoltorio.

```java
String numeroTexto = "150";

int numero = Integer.parseInt(numeroTexto);

double decimal = Double.parseDouble("25.5");
```

### Conversión de números a cadenas

```java
int edad = 20;

String texto = String.valueOf(edad);
```

---

## 6. OPERADORES

Los operadores permiten realizar operaciones matemáticas, comparaciones y evaluaciones lógicas.

### Operadores aritméticos

| Operador | Función | Ejemplo |
|---|---|---|
| `+` | Suma | `10 + 5` |
| `-` | Resta | `10 - 5` |
| `*` | Multiplicación | `10 * 5` |
| `/` | División | `10 / 5` |
| `%` | Módulo o resto | `10 % 3` |

### Operadores de asignación

| Operador | Función | Ejemplo |
|---|---|---|
| `=` | Asignación | `x = 10` |
| `+=` | Suma y asigna | `x += 5` |
| `-=` | Resta y asigna | `x -= 5` |
| `*=` | Multiplica y asigna | `x *= 2` |
| `/=` | Divide y asigna | `x /= 2` |
| `%=` | Calcula el resto y asigna | `x %= 3` |

### Operadores de comparación

| Operador | Función |
|---|---|
| `==` | Igualdad. |
| `!=` | Diferente. |
| `>` | Mayor que. |
| `<` | Menor que. |
| `>=` | Mayor o igual que. |
| `<=` | Menor o igual que. |

### Operadores lógicos

| Operador | Función |
|---|---|
| `&&` | AND: ambas condiciones deben ser verdaderas. |
| `||` | OR: al menos una condición debe ser verdadera. |
| `!` | NOT: invierte el valor lógico. |

### Operadores de incremento y decremento

```java
int numero = 5;

numero++;

numero--;

++numero;

--numero;
```

- `++`: incrementa el valor en una unidad.
- `--`: disminuye el valor en una unidad.

### Operador ternario

Permite evaluar una condición y seleccionar uno de dos valores.

```java
int edad = 20;

String resultado = edad >= 18 ? "Mayor de edad" : "Menor de edad";
```

---

## 7. ENTRADA Y SALIDA DE DATOS

Java permite mostrar información mediante `System.out` y recibir datos del usuario mediante diferentes herramientas.

### Salida de datos

**System.out.print():**

Imprime información sin añadir un salto de línea.

```java
System.out.print("Hola ");
System.out.print("mundo");
```

**System.out.println():**

Imprime información y añade un salto de línea.

```java
System.out.println("Hola, mundo");
```

**System.out.printf():**

Permite mostrar información utilizando formatos.

```java
String nombre = "Juan";
int edad = 20;

System.out.printf("Nombre: %s | Edad: %d%n", nombre, edad);
```

### Entrada de datos mediante Scanner

La clase `Scanner` permite leer datos introducidos por el usuario.

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        System.out.print("Introduce tu nombre: ");

        String nombre = entrada.nextLine();

        System.out.println("Hola, " + nombre);

        entrada.close();

    }

}
```

### Métodos de Scanner

| Método | Función |
|---|---|
| `next()` | Lee una palabra. |
| `nextLine()` | Lee una línea completa. |
| `nextInt()` | Lee un entero. |
| `nextDouble()` | Lee un decimal. |
| `nextFloat()` | Lee un número float. |
| `nextLong()` | Lee un número long. |
| `nextBoolean()` | Lee un valor booleano. |

**Importante:** al combinar métodos como `nextInt()` y `nextLine()`, puede ser necesario consumir el salto de línea pendiente para evitar lecturas vacías inesperadas.

---

## 8. ESTRUCTURAS CONDICIONALES

Las estructuras condicionales permiten ejecutar diferentes instrucciones dependiendo de una condición.

### if

Ejecuta un bloque cuando la condición es verdadera.

```java
int edad = 20;

if (edad >= 18) {

    System.out.println("Mayor de edad");

}
```

### if - else

Permite ejecutar un bloque alternativo cuando la condición no se cumple.

```java
int edad = 16;

if (edad >= 18) {

    System.out.println("Mayor de edad");

} else {

    System.out.println("Menor de edad");

}
```

### if - else if - else

Permite evaluar varias condiciones.

```java
int nota = 85;

if (nota >= 90) {

    System.out.println("Excelente");

} else if (nota >= 70) {

    System.out.println("Aprobado");

} else {

    System.out.println("Reprobado");

}
```

### switch

Permite ejecutar diferentes bloques según el valor de una expresión.

```java
int dia = 2;

switch (dia) {

    case 1:
        System.out.println("Lunes");
        break;

    case 2:
        System.out.println("Martes");
        break;

    case 3:
        System.out.println("Miércoles");
        break;

    default:
        System.out.println("Día no válido");

}
```

### Switch moderno

Java también permite utilizar expresiones `switch`.

```java
int dia = 2;

String nombreDia = switch (dia) {

    case 1 -> "Lunes";
    case 2 -> "Martes";
    case 3 -> "Miércoles";
    default -> "Día no válido";

};

System.out.println(nombreDia);
```

---

## 9. ESTRUCTURAS REPETITIVAS

Los bucles permiten ejecutar un bloque de instrucciones varias veces.

### while

Ejecuta un bloque mientras la condición sea verdadera.

```java
int contador = 1;

while (contador <= 5) {

    System.out.println(contador);

    contador++;

}
```

### do - while

Ejecuta el bloque al menos una vez antes de comprobar la condición.

```java
int contador = 1;

do {

    System.out.println(contador);

    contador++;

} while (contador <= 5);
```

### for

Se utiliza cuando se conoce o controla el número de iteraciones.

```java
for (int i = 1; i <= 5; i++) {

    System.out.println(i);

}
```

### for-each

Permite recorrer los elementos de un arreglo o colección.

```java
int[] numeros = {10, 20, 30, 40};

for (int numero : numeros) {

    System.out.println(numero);

}
```

### break y continue

**break:** termina inmediatamente el bucle.

```java
for (int i = 1; i <= 10; i++) {

    if (i == 5) {
        break;
    }

    System.out.println(i);

}
```

**continue:** salta la iteración actual y continúa con la siguiente.

```java
for (int i = 1; i <= 5; i++) {

    if (i == 3) {
        continue;
    }

    System.out.println(i);

}
```

---

## 10. ARREGLOS

Los arreglos (arrays) permiten almacenar varios elementos del mismo tipo en una estructura de tamaño fijo.

### Declaración

```java
int[] numeros;
```

### Inicialización

```java
int[] numeros = {10, 20, 30, 40};
```

### Declaración con tamaño definido

```java
int[] edades = new int[5];
```

En este caso, el arreglo contiene cinco posiciones inicializadas con el valor predeterminado del tipo de dato.

### Acceso a los elementos

Los índices de los arreglos comienzan en cero.

```java
int[] numeros = {10, 20, 30};

System.out.println(numeros[0]);

System.out.println(numeros[1]);

System.out.println(numeros[2]);
```

### Modificación de elementos

```java
int[] numeros = {10, 20, 30};

numeros[0] = 100;
```

### Propiedad length

Permite conocer la cantidad de posiciones del arreglo.

```java
int[] numeros = {10, 20, 30};

System.out.println(numeros.length);
```

### Arreglos multidimensionales

Permiten almacenar arreglos dentro de otros arreglos.

```java
int[][] matriz = {

    {1, 2, 3},

    {4, 5, 6},

    {7, 8, 9}

};
```

Acceso a un elemento:

```java
System.out.println(matriz[0][1]);
```

Resultado:

```text
2
```

### Recorrer un arreglo

```java
int[] numeros = {10, 20, 30};

for (int i = 0; i < numeros.length; i++) {

    System.out.println(numeros[i]);

}
```

---

## 11. CADENAS DE CARACTERES

La clase `String` permite trabajar con cadenas de texto.

En Java, los objetos `String` son inmutables: sus caracteres no se modifican directamente; las operaciones generan nuevas cadenas.

### Declaración

```java
String nombre = "Juan";

String apellido = "Cuevas";
```

### Concatenación

Permite unir cadenas de texto.

```java
String nombreCompleto = nombre + " " + apellido;
```

### Métodos principales de String

| Método | Función |
|---|---|
| `length()` | Devuelve la longitud de la cadena. |
| `charAt()` | Obtiene el carácter de una posición. |
| `substring()` | Extrae una parte de la cadena. |
| `toUpperCase()` | Convierte el texto a mayúsculas. |
| `toLowerCase()` | Convierte el texto a minúsculas. |
| `trim()` | Elimina espacios al principio y al final. |
| `contains()` | Comprueba si contiene una secuencia de caracteres. |
| `equals()` | Compara el contenido de dos cadenas. |
| `equalsIgnoreCase()` | Compara ignorando mayúsculas y minúsculas. |
| `replace()` | Reemplaza caracteres o secuencias. |
| `isEmpty()` | Comprueba si la cadena está vacía. |
| `isBlank()` | Comprueba si está vacía o contiene solo espacios en blanco. |
| `startsWith()` | Comprueba cómo comienza una cadena. |
| `endsWith()` | Comprueba cómo termina una cadena. |

### Ejemplo:

```java
String texto = "Aprendiendo Java";

System.out.println(texto.length());

System.out.println(texto.toUpperCase());

System.out.println(texto.contains("Java"));

System.out.println(texto.substring(0, 11));
```

### Comparación de cadenas

Para comparar el contenido de dos cadenas se utiliza `equals()`.

```java
String palabra1 = "Java";

String palabra2 = "Java";

System.out.println(palabra1.equals(palabra2));
```

No se debe utilizar `==` como sustituto de `equals()` para comparar el contenido de cadenas, porque `==` compara referencias de objetos.

---

## 12. MÉTODOS Y FUNCIONES

Los métodos permiten agrupar instrucciones para reutilizar código y organizar la lógica de un programa.

En Java, las funciones se definen dentro de clases o interfaces y se denominan métodos.

### Declaración de un método

```java
public static void saludar() {

    System.out.println("Hola, mundo");

}
```

### Llamada a un método

```java
public class Main {

    public static void saludar() {

        System.out.println("Hola, mundo");

    }

    public static void main(String[] args) {

        saludar();

    }

}
```

### Métodos con parámetros

Los parámetros permiten enviar información a un método.

```java
public static void saludar(String nombre) {

    System.out.println("Hola, " + nombre);

}
```

Llamada:

```java
saludar("Juan");
```

### Métodos con retorno

Permiten devolver un resultado mediante `return`.

```java
public static int sumar(int a, int b) {

    return a + b;

}
```

Uso:

```java
int resultado = sumar(10, 20);

System.out.println(resultado);
```

### Sobrecarga de métodos (Overloading)

Permite declarar varios métodos con el mismo nombre, siempre que tengan diferentes listas de parámetros.

```java
public static int sumar(int a, int b) {

    return a + b;

}

public static double sumar(double a, double b) {

    return a + b;

}
```

### Métodos recursivos

Son métodos que se llaman a sí mismos para resolver un problema.

```java
public static int factorial(int numero) {

    if (numero <= 1) {
        return 1;
    }

    return numero * factorial(numero - 1);

}
```

---

## 13. PROGRAMACIÓN ORIENTADA A OBJETOS

Java utiliza la programación orientada a objetos (POO) como uno de sus principales paradigmas.

Este enfoque permite organizar el código mediante clases y objetos.

### Clases

Una clase es una estructura que define las características y comportamientos que tendrán sus objetos.

```java
public class Persona {

    String nombre;

    int edad;

    void saludar() {

        System.out.println("Hola, soy " + nombre);

    }

}
```

### Objetos

Un objeto es una instancia de una clase.

```java
Persona persona1 = new Persona();

persona1.nombre = "Juan";

persona1.edad = 20;

persona1.saludar();
```

### Constructores

Los constructores permiten inicializar los objetos cuando se crean.

```java
public class Persona {

    String nombre;

    int edad;

    public Persona(String nombre, int edad) {

        this.nombre = nombre;

        this.edad = edad;

    }

}
```

Creación del objeto:

```java
Persona persona1 = new Persona("Juan", 20);
```

### La palabra reservada this

Se utiliza para hacer referencia al objeto actual.

```java
public class Persona {

    String nombre;

    public Persona(String nombre) {

        this.nombre = nombre;

    }

}
```

### Los cuatro pilares de la POO

| Pilar | Descripción |
|---|---|
| Encapsulamiento | Protege y controla el acceso a los datos de un objeto. |
| Abstracción | Representa las características esenciales de un objeto. |
| Herencia | Permite crear clases basadas en otras clases. |
| Polimorfismo | Permite utilizar una misma interfaz con diferentes implementaciones. |

---

## 14. MODIFICADORES DE ACCESO

Los modificadores de acceso permiten controlar la visibilidad de clases, atributos, métodos y constructores.

### Tipos principales

| Modificador | Acceso |
|---|---|
| `public` | Accesible desde cualquier clase. |
| `private` | Accesible únicamente dentro de la clase donde se declara. |
| `protected` | Accesible dentro del mismo paquete y desde subclases, con las reglas propias de Java. |
| Sin modificador | Acceso de paquete: disponible dentro del mismo paquete. |

### Encapsulamiento

Consiste en proteger los atributos de una clase y controlar su acceso mediante métodos.

```java
public class Persona {

    private String nombre;

    public void setNombre(String nombre) {

        this.nombre = nombre;

    }

    public String getNombre() {

        return nombre;

    }

}
```

Uso:

```java
Persona persona = new Persona();

persona.setNombre("Juan");

System.out.println(persona.getNombre());
```

- `getNombre()`: permite consultar el valor.
- `setNombre()`: permite modificar el valor.

---

## 15. HERENCIA Y POLIMORFISMO

### Herencia

Permite que una clase herede atributos y métodos de otra clase mediante la palabra reservada `extends`.

```java
public class Animal {

    public void comer() {

        System.out.println("El animal está comiendo");

    }

}
```

Clase derivada:

```java
public class Perro extends Animal {

    public void ladrar() {

        System.out.println("Guau");

    }

}
```

Uso:

```java
Perro perro = new Perro();

perro.comer();

perro.ladrar();
```

### Sobrescritura de métodos (Overriding)

Permite que una subclase proporcione una implementación propia de un método heredado.

```java
public class Animal {

    public void sonido() {

        System.out.println("Sonido de animal");

    }

}
```

```java
public class Perro extends Animal {

    @Override
    public void sonido() {

        System.out.println("Guau");

    }

}
```

### Polimorfismo

Permite utilizar una referencia de una clase base para representar objetos de diferentes subclases.

```java
Animal animal = new Perro();

animal.sonido();
```

Aunque la referencia es de tipo `Animal`, se ejecuta la implementación de `Perro`.

---

## 16. INTERFACES Y CLASES ABSTRACTAS

### Interfaces

Una interfaz define un contrato que las clases pueden implementar.

```java
public interface Vehiculo {

    void arrancar();

    void detener();

}
```

Implementación:

```java
public class Moto implements Vehiculo {

    @Override
    public void arrancar() {

        System.out.println("La moto ha arrancado");

    }

    @Override
    public void detener() {

        System.out.println("La moto se ha detenido");

    }

}
```

### Clases abstractas

Son clases que no pueden instanciarse directamente y pueden definir métodos abstractos y métodos con implementación.

```java
public abstract class Animal {

    public abstract void sonido();

    public void dormir() {

        System.out.println("El animal está durmiendo");

    }

}
```

Implementación:

```java
public class Gato extends Animal {

    @Override
    public void sonido() {

        System.out.println("Miau");

    }

}
```

### Diferencias principales

| Característica | Interfaz | Clase abstracta |
|---|---|---|
| Declaración | `interface` | `abstract class` |
| Implementación | `implements` | `extends` |
| Instanciación directa | No | No |
| Métodos abstractos | Sí | Sí |
| Métodos con implementación | Sí | Sí |
| Atributos de instancia | No | Sí |
| Constructores | No | Sí |
| Herencia múltiple | Una clase puede implementar varias interfaces. | Una clase solo puede extender una clase. |

---

## 17. COLECCIONES

Las colecciones permiten almacenar y administrar grupos de objetos de manera flexible.

Java proporciona el Java Collections Framework, que incluye interfaces y clases para trabajar con diferentes estructuras de datos.

### List

Permite almacenar elementos en una secuencia, mantener su orden y admitir elementos duplicados.

Ejemplo con ArrayList:

```java
import java.util.ArrayList;

public class Main {

    public static void main(String[] args) {

        ArrayList<String> nombres = new ArrayList<>();

        nombres.add("Juan");

        nombres.add("Pedro");

        nombres.add("María");

        System.out.println(nombres);

    }

}
```

### Métodos de ArrayList

| Método | Función |
|---|---|
| `add()` | Añade un elemento. |
| `get()` | Obtiene un elemento por índice. |
| `set()` | Modifica un elemento. |
| `remove()` | Elimina un elemento. |
| `size()` | Devuelve la cantidad de elementos. |
| `contains()` | Comprueba si contiene un elemento. |
| `clear()` | Elimina todos los elementos. |
| `isEmpty()` | Comprueba si está vacía. |

### Set

Almacena elementos únicos, sin duplicados.

```java
import java.util.HashSet;

HashSet<String> lenguajes = new HashSet<>();

lenguajes.add("Java");

lenguajes.add("Python");

lenguajes.add("Java");
```

En este ejemplo, el segundo registro de `Java` no se incorpora porque ya existe.

### Map

Almacena información mediante pares de clave y valor.

```java
import java.util.HashMap;

HashMap<String, Integer> edades = new HashMap<>();

edades.put("Juan", 20);

edades.put("Pedro", 25);

System.out.println(edades.get("Juan"));
```

### Estructuras principales

| Interfaz | Implementación habitual | Característica |
|---|---|---|
| `List` | `ArrayList` | Secuencia de elementos. |
| `List` | `LinkedList` | Lista enlazada. |
| `Set` | `HashSet` | Elementos únicos sin orden garantizado. |
| `Set` | `TreeSet` | Elementos únicos ordenados. |
| `Map` | `HashMap` | Pares clave-valor sin orden garantizado. |
| `Map` | `TreeMap` | Pares clave-valor ordenados por clave. |

---

## 18. MANEJO DE EXCEPCIONES

Las excepciones representan situaciones anormales que pueden producirse durante la ejecución de un programa.

Java proporciona mecanismos para detectar y controlar estos errores.

### try - catch

Permite ejecutar instrucciones y capturar excepciones.

```java
try {

    int resultado = 10 / 0;

} catch (ArithmeticException e) {

    System.out.println("No es posible dividir entre cero");

}
```

### finally

El bloque `finally` se ejecuta después del bloque `try` y de los posibles bloques `catch`, incluso cuando se produce una excepción.

```java
try {

    System.out.println("Ejecutando operación");

} catch (Exception e) {

    System.out.println("Se produjo un error");

} finally {

    System.out.println("Finalizando proceso");

}
```

### throw

Permite lanzar una excepción de manera explícita.

```java
public static void validarEdad(int edad) {

    if (edad < 18) {

        throw new IllegalArgumentException("Edad no válida");

    }

}
```

### throws

Permite declarar que un método puede propagar determinadas excepciones.

```java
import java.io.IOException;

public static void leerArchivo() throws IOException {

    // Operaciones de lectura

}
```

### Tipos de excepciones

| Tipo | Descripción |
|---|---|
| Checked Exceptions | Deben capturarse o declararse cuando corresponda. |
| Unchecked Exceptions | Excepciones derivadas de `RuntimeException`. |
| Errors | Problemas graves relacionados normalmente con el entorno de ejecución. |

---

## 19. OPERACIONES CON ARCHIVOS

Java permite crear, leer, escribir y administrar archivos.

Para trabajar con archivos modernos se recomienda conocer las clases de `java.nio.file`.

### Crear un archivo

```java
import java.nio.file.Files;
import java.nio.file.Path;

public class Main {

    public static void main(String[] args) throws Exception {

        Path archivo = Path.of("datos.txt");

        Files.createFile(archivo);

    }

}
```

### Escribir en un archivo

```java
import java.nio.file.Files;
import java.nio.file.Path;

public class Main {

    public static void main(String[] args) throws Exception {

        Path archivo = Path.of("datos.txt");

        Files.writeString(archivo, "Aprendiendo Java");

    }

}
```

### Leer un archivo

```java
import java.nio.file.Files;
import java.nio.file.Path;

public class Main {

    public static void main(String[] args) throws Exception {

        Path archivo = Path.of("datos.txt");

        String contenido = Files.readString(archivo);

        System.out.println(contenido);

    }

}
```

### Clases importantes

| Clase | Función |
|---|---|
| `File` | Representa archivos y directorios mediante la API clásica. |
| `Path` | Representa una ruta de archivo. |
| `Files` | Proporciona operaciones sobre archivos y directorios. |
| `FileReader` | Permite leer archivos de texto. |
| `FileWriter` | Permite escribir archivos de texto. |
| `BufferedReader` | Facilita la lectura eficiente de texto. |
| `BufferedWriter` | Facilita la escritura eficiente de texto. |

---

## 20. PAQUETES E IMPORTACIONES

Los paquetes permiten organizar las clases y evitar conflictos entre nombres.

### Declaración de un paquete

```java
package com.proyecto.usuarios;

public class Persona {

}
```

La declaración `package` debe aparecer al principio del archivo, antes de las declaraciones de tipos.

### Importación de clases

Permite utilizar clases de otros paquetes sin escribir su nombre completamente cualificado.

```java
import java.util.Scanner;

import java.util.ArrayList;
```

### Importación de un paquete

```java
import java.util.*;
```

Esta instrucción permite utilizar los tipos accesibles de ese paquete, pero no importa automáticamente sus subpaquetes.

### Ejemplo de organización

```text
src/
│
└── main/
    └── java/
        └── com/
            └── proyecto/
                │
                ├── Main.java
                │
                ├── modelos/
                │   └── Persona.java
                │
                └── servicios/
                    └── UsuarioService.java
```

---

## 21. EXPRESIONES LAMBDA

Las expresiones lambda permiten representar funciones de manera concisa y se utilizan principalmente con interfaces funcionales.

### Sintaxis general

```java
(parametros) -> expresion
```

### Ejemplo básico

```java
interface Operacion {

    int ejecutar(int a, int b);

}

public class Main {

    public static void main(String[] args) {

        Operacion suma = (a, b) -> a + b;

        System.out.println(suma.ejecutar(10, 20));

    }

}
```

### Uso con listas

```java
import java.util.ArrayList;

ArrayList<String> nombres = new ArrayList<>();

nombres.add("Juan");

nombres.add("Pedro");

nombres.add("María");

nombres.forEach(nombre -> System.out.println(nombre));
```

### Conceptos relacionados

- `->`: operador utilizado en las expresiones lambda.
- Interfaz funcional: interfaz con un único método abstracto.
- `@FunctionalInterface`: anotación que permite indicar que una interfaz está diseñada para ser funcional.
- Method reference (`::`): permite hacer referencia a métodos existentes.

Ejemplo de referencia a método:

```java
nombres.forEach(System.out::println);
```

---

## 22. BUENAS PRÁCTICAS

Para desarrollar aplicaciones Java organizadas, mantenibles y fáciles de comprender, es recomendable seguir ciertas convenciones.

### Recomendaciones

1. Utilizar nombres descriptivos para variables y métodos.
2. Aplicar `camelCase` en variables y métodos.
3. Aplicar `PascalCase` en nombres de clases.
4. Utilizar mayúsculas y guiones bajos para constantes.
5. Declarar atributos como `private` cuando corresponda.
6. Evitar repetir código innecesariamente.
7. Dividir los programas en métodos con responsabilidades claras.
8. Utilizar excepciones específicas.
9. Cerrar los recursos correctamente.
10. Preferir las interfaces de colecciones frente a depender innecesariamente de implementaciones concretas.
11. Evitar utilizar `==` para comparar el contenido de objetos.
12. Documentar las clases y métodos cuando sea necesario.

### Convenciones de nombres

| Elemento | Convención | Ejemplo |
|---|---|---|
| Clase | PascalCase | `UsuarioService` |
| Variable | camelCase | `nombreUsuario` |
| Método | camelCase | `calcularTotal()` |
| Constante | MAYÚSCULAS | `VALOR_MAXIMO` |
| Paquete | Minúsculas | `com.proyecto.usuarios` |

---

## 23. ESTRUCTURA DE UN PROYECTO JAVA

Una estructura organizada permite separar responsabilidades y facilitar el mantenimiento de las aplicaciones.

### Ejemplo de organización

```text
PROYECTO-JAVA/
│
├── src/
│   ├── main/
│   │   └── java/
│   │       └── com/
│   │           └── proyecto/
│   │               │
│   │               ├── Main.java
│   │               │
│   │               ├── modelos/
│   │               │   └── Usuario.java
│   │               │
│   │               ├── servicios/
│   │               │   └── UsuarioService.java
│   │               │
│   │               └── utilidades/
│   │                   └── Validador.java
│   │
│   └── test/
│       └── java/
│
├── pom.xml
│
└── README.md
```

### Descripción

| Elemento | Función |
|---|---|
| `src/main/java` | Contiene el código fuente principal. |
| `src/test/java` | Contiene las pruebas automatizadas. |
| `modelos/` | Almacena clases que representan entidades y datos. |
| `servicios/` | Contiene lógica y operaciones de negocio. |
| `utilidades/` | Agrupa herramientas reutilizables. |
| `pom.xml` | Archivo de configuración de Maven. |
| `README.md` | Documentación del proyecto. |

### Compilación y ejecución básica

Compilar un archivo:

```bash
javac Main.java
```

Ejecutar el programa:

```bash
java Main
```

También es posible ejecutar directamente un archivo fuente con versiones modernas del entorno Java:

```bash
java Main.java
```

---

## 📚 RECURSOS DE CONSULTA

- [Documentación oficial de Java](https://docs.oracle.com/en/java/)
- [Java Language Specification](https://docs.oracle.com/javase/specs/)
- [Dev.java — Aprender Java](https://dev.java/learn/)
- [Oracle Java Tutorials](https://docs.oracle.com/javase/tutorial/)

---

## 🎯 OBJETIVO DEL REPOSITORIO

Construir una referencia organizada de Java que permita consultar sus fundamentos, comprender sus estructuras y reforzar los conocimientos necesarios para desarrollar aplicaciones mediante programación estructurada y orientada a objetos.

**Aprendiendo · Practicando · Construyendo.**
