---
layout: post
title: Tema 3 de Acceso a Datos
---
### Funciones
Este es mi resumen del Tema 3 de Acceso a Datos, del 2º curso del Ciclo de Desarrollo de Aplicaciones Multiplataforma.

## Funciones
Las funciones se usan dentro de expresiones y actúan con los valores de las columnas, variables o constantes.
Se utilizan en: *cláusulas SELECT*, *cláusulas WHERE*, *cláusulas ORDER BY*.
  - [Funciones aritméticas](#F1)
  - [Funciones de cadenas de caracteres](#F2)
  - [Funciones de manejo de fechas](#F3)
  - [Funciones de conversión](#F4)
  - [Otras funciones](#F5)

### Funciones aritméticas: <a id="F1"></a>
Las funciones aritméticas trabajan con datos de tipo numérico *NUMBER*.
- [Funciones de valores simples](#F1a)
- [Funciones de grupos de valores](#F1b)
- [Funciones de lista](#F1c)

#### Funciones de valores simples: <a id="F1a"></a>

FUNCIÓN | DESCRIPCIÓN
-- | --
**ABS**(n) | Devuelve el valor absoluto de _n_.
**CEIL**(n) | Obtiene el valor entero inmediatamente superior o igual a _n_.
**FLOOR**(n) | Obtiene el valor entero inmediatamente inferior o igual a _n_.
**MOD**(m, n) | Devuelve e resto resultante de dividir _m_ entre _n_.
**NVL**(valor, expresión) | Sustituye un valor nulo por otro valor.
**POWER**(n, e) | Calcula la potencia de un número. Devuelve el valor de *n* elevado a *e*.
**ROUND**(n [,d]) | Redondea un número *n* con el número de dígitos de precisión indicado por *d*. Si *d* es negativo, el redondeo de dígitos se lleva a cabo a la izquierda del punto decimal.
**SIGN**(valor) | Esta función indica el signo del *valor*. Si es menor que 0 devuelve -1 y si es mayor devuelve 1.
**SQRT**(n) | Devuelve la raíz cuadrada de *n*.
**TRUNC**(n [,d]) | Devuelve un número *n* truncado a *d* decimales. Si *d* es negativo trunca por la izquierda del punto decimal.
**VARIANCE**(valor) | Devuelve varianza de un conjunto de valores.


#### Funciones de grupos de valores: <a id="F1b"></a>
FUNCIÓN | DESCRIPCIÓN
-- | --
**AVG**(n) | Calcula el valor medio de *n* ignorando los valores nulos.
**COUNT**(expresión)</br>**COUNT**(*) | Cuenta el número de veces que la expresión evalúa algún dato con valor no nulo. La opción * cuenta todas las filas seleccionadas.
**MAX**(expresión) | Calcula el máximo valor de la expresión.
**MIN**(expresión) | Calcula el mínimo valor de la expresión.
**SUM**(expresión) | Calcula la suma de valores la expresión.
Si *COUNT* recibe como argumento una expresión o columna, ésta podrá ir precedida de las cláusulas *ALL* o *DISTINCT*.

#### Funciones de lista: <a id="F1c"></a>
FUNCIÓN | DESCRIPCIÓN
-- | --
**GREATEST**(valor1, valor2, ...) | Obtiene el mayor valor de la lista.
**LEAST**(valor1, valor2, ...) | Obtiene el menor valor de la lista.

### Funciones de cadenas de caracteres: <a id="F2"></a>
Estas funciones trabajan con datos de tipo *CHAR* o *VARCHAR2*. Estos datos incluyen cualquier carácter alfanumérico: letras, números y caracteres especiales. Los literales se deben encerrar entre comillas simples.
- [Funciones que devuelven valores carácter](#F2a)
- [Funciones que devuelven valores numéricos](#F2b)

#### Funciones que devuelven valores carácter: <a id="F2a"></a>

FUNCIÓN | DESCRIPCIÓN
-- | --
**CHR**(n) | Devuelve el carácter cuyo valor en binario es equivalente a *n*.
**CONCAT**(cad1, cad2) | Devuelve *cad1* concatenada con *cad2*.
**LOWER**(cad) | Devuelve *cad* en minúsculas.
**UPPER**(cad) | Devuelve *cad* en mayúsculas.
**INITCAP**(cad) | Devuelve *cad* en tipo título.
**LPAD**(cad1, n, [,cad2]) | Añade caracteres a la izquierda de la cadena, hasta que tenga una cierta longitud.
**RPAD**(cad1, n, [,cad2]) | Añade caracteres a la derecha de la cadena, hasta que tenga una cierta longitud.
**LTRIM**(cad, n, [,set]) | Suprime un conjunto de caracteres a la izquierda de la cadena.
**RTRIM**(cad, n, [,set]) | Suprime un conjunto de caracteres a la derecha de la cadena.
**REPLACE**(cad, cadena_busqueda [, cadena_sustitución]) | Sustituye un carácter o caracteres de una cadena con 0 o más caracteres.
**SUBSTR**(cad, m, [,n]) | Obtiene parte de una cadena.
**TRANSLATE**(cad1, cad2, cad3) | Convierte caracteres de una cadena en caracteres diferentes, según un plan de sustitución marcado por el usuario.
**SOUNDEX**(cadena) | Devuelve una cadena de caracteres que contiene la representación fonética de *cadena*.

#### Funciones que devuelven valores numéricos: <a id="F2b"></a>

FUNCIÓN | DESCRIPCIÓN
-- | --
**ASCII**(cad) | Devuelve el valor ASCII de la primera letra de la cadena *cad*.
**INSTR**(cad1, cad2 [,comienzo[,m]]) | Busca un conjunto de caracteres en una cadena. Devuelve la posición de la m_ésima ocurrencia de *cad2* en *cad1*, empezando la búsqueda en la posición *comienzo*.
**LENGTH**(cad) | Devuelve el número de caracteres de *cad*.

### Funciones para el manejo de fechas: <a id="F3"></a>
El tipo de datos ***DATE*** se almacena en un formato especial que incluye *mes/día/año/hora/minutos/segundos*. Tiene un formato por omisión: *'DD-MM-YY'*, pero con la función *TO_CHAR* es posible mostrar las fechas de cualquier modo. Los literales de fecha deben encerrarse entre comillas simples.

FUNCIÓN | DESCRIPCIÓN
-- | --
**SYSDATE** | devuelve la fecha del sistema.
**ADD_MONTHS**(fecha, n) | Devuelve *fecha* incrementada en *n* meses.
**LAST_DAY**(fecha) | Devuelve la fecha del último día del mes que contiene *fecha*.
**MONTHS_BETWEEN**(fecha1, fecha2) | Devuelve la diferencia en meses entre *fecha1* y *fecha2*. Puede ser un número decimal.
**NEXT_DAY**(fecha, cad) | Devuelve la fecha del primer día de la semana indicado por *cad* después de la fecha indicada por *fecha*.

### Funciones de conversión: <a id="F4"></a>
Estas funciones transforman un tipo de dato en otro.

FUNCIÓN | DESCRIPCIÓN
-- | --
**TO_CHAR**(fecha, 'formato') | Convierte *fecha* (de tipo DATE) a tipo VARCHAR2 en el *formato* especificado.
**TO_NUMBER**(cadena[, formato]) | Convierte *cadena* a tipo NUMBER según el *formato* especificado.

### Otras funciones: <a id="F5"></a>

FUNCIÓN | DESCRIPCIÓN
-- | --
**DECODE**(var; val1, cod1, val2, cod2..., valor_por_defecto) | Esta función sustituye un valor por otro. Si *var* es igual a cualquier valor de la lista (*val1*, *val2*,...), devuelve el correspondiente código (*cod1*,*cod2*,...). En caso contrario se obtiene el valor por defecto *val*.
**VSIZE**(expresión) | Devuelve el número de bytes que ocupa *expresión*. Si expresión es nulo, la función devuelve nulo.
**DUMP**(cadena[, formato [,comienzo[, longitud]]]) | Visualiza el valor de *cadena*, que puede ser un literal o una expresión, en formato de datos internos, en ASCII, octal, decimal, hexadecimal o en formato de carácter. Por defecto, el formato es ASCII o EBCDIC, lo que depende de la máquina.
**USER** | Devuelve el nombre del usuario actual.
**UID** | Devuelve el identificador del usuario actual. Al crear un usuario, Oracle le asigna un número. Este número identifica a cada usuario y es único en la base de datos. (\*)
(\*) La orden ***SHOW USER*** muestra qué usuario somos:

 ```
