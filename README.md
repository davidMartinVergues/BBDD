# Curso de base de datos

## DBMS - Database management system

Significa "Sistema de gestión de bases de datos". En resumen, un DBMS es un programa de base de datos. Técnicamente hablando, es un sistema de software que utiliza un método estándar de catalogación, recuperación y ejecución de consultas sobre datos. El DBMS administra los datos entrantes, los organiza y proporciona formas para que los usuarios u otros programas modifiquen o extraigan los datos.

Algunos ejemplos de DBMS incluyen MySQL, PostgreSQL, Microsoft Access, SQL Server, FileMaker, Oracle, RDBMS, dBASE, Clipper y FoxPro. Dado que hay tantos sistemas de gestión de bases de datos disponibles, es importante que haya una manera de comunicarse entre ellos. Por esta razón, la mayoría del software de base de datos viene con una conectividad de base de datos abierta (ODBC) controlador que permite que la base de datos se integre con otras bases de datos. Por ejemplo, las instrucciones SQL comunes como SELECT e INSERT se traducen de la sintaxis patentada de un programa a una sintaxis que otras bases de datos pueden entender.

## RDBMS

Significa "Sistema de gestión de bases de datos relacionales". Un RDBMS es un DBMS diseñado específicamente para bases de datos relacionales. Por lo tanto, los RDBMS son un subconjunto de DBMS.

Una base de datos relacional se refiere a un base de datos que almacena datos en un formato estructurado, utilizando filas y a la columnas. Esto facilita la localización y el acceso a valores específicos dentro de la base de datos. Es "relacional" porque los valores dentro de cada mesa están relacionados entre sí. Las tablas también pueden estar relacionadas con otras tablas. La estructura relacional permite ejecutar consultas en varias tablas a la vez.

Mientras que una base de datos relacional describe el tipo de base de datos que administra un RDMBS, el RDBMS se refiere a la base de datos programa sí mismo. Es el software que ejecuta consultas sobre los datos, incluida la adición, actualización y búsqueda de valores. Un RDBMS también puede proporcionar una representación visual de los datos. Por ejemplo, puede mostrar datos en tablas como un hoja de cálculo, lo que le permite ver e incluso editar valores individuales en la tabla. Algunos programas RDMBS le permiten crear formularios que pueden agilizar el ingreso, la edición y la eliminación de datos.

## Relational Data Base - RDB

Están formadas por:

1. entidad
   
Son objetos de ls bbdd que representa algo del mundo real. Las entidades tiene:

- `atributos`, es lo q las definen como entidad
  - un laptop (entidad) tiene atributos:
    - pantalla
    - color
    - año
    - antiguedad - se puede inferir a partir del año se representa en discontinuo
    - modelo
    - discoduro - attr multivaluado, puede haber más de un disco duro
    - método de entrada - attr compuesto pq tiene a su vez otros atributos como
      - trackpad
      - teclado
    - numero de serie - attri primary key - nos ayuda a identificar de manera única a la entidad


![not found](img/2.png)

De primary key hay de dos tipo:

1. naturales    => pq son inherentes a la entidad pej número de serie del laptop o el ISBAN de un libro
2. artificiañes => clave asignada de manera arbitraria como un campo id

Hay dos tipos de entidades:

1. fuertes  => ueden existir por si mismas (se representan como un rectángulo)
2. débiles  => necesitan a una entidad fuerte para existir (se representan con doble rectángulo)

Un ejemplo de esto puede ser entidad fuerte libro y ejemplar como entidad débil. Existe un libro en sí mismo pero para la entidad ejemplar necesitamos que exista el libro.

Las entidades débiles pueden serlo por:

1. identidad    => se diferencian entre sí por la clave de su entidad fuerte, para diferenciar los diferentes ejemplares de libros necesitamos la PK de libro

2. existencia   => aunq creemos una PK para los ejemplares y por lo tanto ya no son débiles por identidad siguen siendo débiles por existencia pq no puede existir un ejemplar sin un libro.

![not found](img/3.png)

La nomenglatura para poder representar todo lo comentado es la siguiente

![not found](img/1.jpg)
