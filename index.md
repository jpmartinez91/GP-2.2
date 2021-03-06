# Procesamiento de Lenguaje Natural

![PLN](https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcTMSPSC0ooQpZVdv71LEvR3RMilxk3UGeLEVgZ2rwA6sg5jNdiC)

El procesamiento de Lenguaje Natural o PLN es un campo de las ciencias de la computación, inteligencia artificial y lingüística que estudia las interacciones entre las computadoras y el lenguaje humano. El PLN no trata de la comunicación por medio de lenguajes naturales de una forma abstracta, sino de diseñar mecanismos para comunicarse que sean eficaces computacionalmente —que se puedan realizar por medio de programas que ejecuten o simulen la comunicación

## Procesamiento Manual

### Normalizado de texto

 1. Elimnar para vacias como por ejemplo: un, una, la. Son palabras que impiden el correcto armado de corpus (texto a procesar).
 
 2.Tokenizacion o segmentacion de texto en oraciones. Se refiere a la segmentacion del texto por coma (,) y conjuncion (y/e).
 
```markdown

**Texto original**

Mantenimiento correctivo y preventivo de Pcs, perifericos
hardware, soluciones software, atencion al cliente

**Texto normalizado**

Mantenimiento correctivo
preventivo de Pcs
perifericos hardware
soluciones software
atencion cliente
```

### Etiquetado con Software libre (Online)

El etiquetado del texto parte del tezto normalizado

Se hace uso de la herramienta web [FreeLing 4.0] (http://nlp.lsi.upc.edu/freeling/demo/demo.php), en donde se obtiene una estructura parecida a:

```markdown
Mantenimiento  correctivo
mantenimiento  correctivo
NCMS000        AQ0MS00
------------------------------------
preventivo     de          Pcs
preventivo     de          pcs
NCMS000        SP          NP00000
------------------------------------
perifericos    hardware
perifericos    hardware
AQ0MP00        NCMS000
------------------------------------
soluciones     software
solución       software
NCFP000        NCMN000
------------------------------------
atencion       cliente
atencion       cliente
NCFS000        NCCS000
------------------------------------
```

### Cálculo de coeficiente de Kappa Cohen

El Coeficiente kappa de Cohen mide la concordancia entre dos examinadores en sus correspondientes clasificaciones de N elementos en C categorías

Hay que tener en cuenta que la kappa de Cohen sólo mide el acuerdo entre dos observadores.

### Identificacion del dominio y nivel cognitivo
 
diseñador y administrador de sistemas de comunicación de datos

A partir de una taxonomia:

```markdown
- diseñar
- administrar
```

el domonio y nivel cognitivo es:

```markdown
- crear   5
- crear   5
```

************************************

operación y mantenimiento de sistemas electrónicos


A partir de una taxonomia:

```markdown
- operación 
- mantenimiento
```

el domonio y nivel cognitivo es:

```markdown
- aplicar  3
- evaluar  6
```

### Armado de Ontologia

Para la creacion de la ontologia se partio por la toxonomia de las oraciones tokenizadas.

Se hizo uso del sofware libre "protege' en su version 5.1.0 el cual sirvio para crear la ontologia de los verbos encontrados en los textos procesados.

## Desarrollo aplicacion

### Familiarizacion de libreria NLTK de Python

NLTK es una plataforma líder para la creación de programas de Python para trabajar con los datos del lenguaje humano. Proporciona interfaces fáciles de usar para más de 50 corpus y recursos léxicos como WordNet, junto con un conjunto de bibliotecas de procesamiento de texto para la clasificación, tokenización, derivado, etiquetado, análisis y de razonamiento semántico, contenedores para las bibliotecas de PNL de potencia industrial

```markdown
Instalar NLTK: ejecutar sudo pip install -U nltk
```

Luego se debe descargar los diferentes componentes provistos por NLTK

Desde el interprete de python se debe importar la libreria NLTK y descargar los componentes y corpus necesarios para el trabajo a realizar

```markdown
import nltk

nltk.download()
```

### Familiarizacion de extension Stanford Natural Language Processing Group para NLTK

Dado que NLTK no provee una gama amplia de funcionalidades para el idioma Español, se examino las librerias provistas por [Stanford] (http://nlp.stanford.edu/software/) la cuál potencializa las funcionales de NLTK.

### Normalizado de texto



### Tokenizacion de Oraciones y Palabras



### Etiquetado del texto

Para el etiquetado del texto se parte del texto de un texto de entrenamiento que basicamente fue el etiquetado manual del texto

### Identificacion de oraciones candidatas

La identificacion de las oraciones candidatas se realizo haciendo uso del etiquetado manual del texto del cual se obtuvieron algunos patrones o sintagmas que sirven como punto base para la identificacion de las oraciones. 

### Documentacion de analisis de texto analizados  
