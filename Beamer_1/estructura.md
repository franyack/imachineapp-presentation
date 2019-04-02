SE PUEDEN RECORTAR ALGUNAS DIAPOS PARA TENER UN GAP DE 30" AL MENOS?

Total: (45')

#### Introducción: **(5')**

? Aclarar tipo de audiencia objetivo?
6000 líneas de código, y 120 hojas de informe

 - Intro de deep learning y antecedentes **(2')**
  + Breves conceptos de DL **(1')**
  + Listar antecedentes **(1')**
  	+ Gatos y personas en YouTube (30")
      - “We never told it during the training, ‘This is a cat,'. It basically invented the concept of a cat.” Jeff Dean, the Google fellow.
    + Énfasis en que se hizo mediante sistemas distribuidos
    + AlphaGo (30")
      - DeepMind, una empresa que Google compró por más de U$D 500 millones
      - AlphaGo: DL y RL para aprender el juego de mesa Go. Esa mezcla ahora se considera una verdadera IA.
      - En 2016 le ganó una competencia de 5 juegos a Lee Sodol, uno de los mejores jugadores de Go en el mundo.

 - Listar tools de deep learning **(1')**
  + Pros y Cons de cada uno, revelados en base al uso.
  + Aclarar que cuando se estaba creando Learninspy no había la cantidad de frameworks actuales (e.g. TensorFlow, Neon, Keras)

 - Objetivos **(1')**
   + Casos de aplicación complejos para validar utilidad

 - Introducir lo que se origina en la tesis **(1')**
  + Dos ejes de justificacion
  + Resaltar que se crea un producto de software!
    + Acá aparece el logo

#### Fundamentos teóricos (10')

> IDEA: mostrar todos los componentes de un modelo (e.g. regresion, costo, optimizacion, regularización, etc) sin entrar en detalles teóricos de forma que se entienda cómo se implementa y su funcionamiento de principio a fin (incluso en redes neuronales). Es para entender lo que se debe implementar en un framework

 - Definir aprendizaje maquinal y su clasificacion (1')
  + Quizás la diapositiva de machine learning va antes que la de deep learning

 - Sist de regresion y Sist de clasificación (4')
    + Funcion de regresión (lineal/logística/softmax) (1'30")
      + Ejemplo con softmax
        + Hipotesis
        + Error: Entropía cruzada
    + Comparar métodos de optimización brevemente **(1'30")**
    + Mencionar brevemente las métricas para clasif y regresión **(1')**
      + No mostrar matriz de confusión, pero mencionar que se aplica lo mismo a ella

  - Redes neuronales: **(5')**
    + Introducir redes neuronales, como se arquitectan, func de activ y retropropag (no explicar!) **(1'30")**
      + Acordarse de aclarar q la clasif la hace un softmax
    + Evolución a deep learning (breve) **(1'30")**
    + Aprendizaje no supervisado (breve) **(30")**
    + Autoencoder y SAE (enfasis acá) **(1'30")**
      + Sólo mostrar imágenes, sin texto.


#### Cómputo distribuido: **(6')**

  - Características **(1')**
    + Mecionar solamente, ir rápido
  - Antecedentes de comp distrib (mapreduce, hadoop) (2')
    + Ejemplo de wordcount en MapReduce (1'30")
    + Hadoop (30")
  - Introducir Spark y mencionar conceptos básicos (breve) **(2')**
  - Aplicaciones a deep learning (mencionar) **(1')**
    + Recordar experimento de gatos

#### Learninspy: (12')

  ````
  + Learninspy es un framework (30")
    + Facilita trabajar con tecnologías complejas, en este caso Spark y SciPy por ejemplo.
    + Reutilización de módulos o componentes,
    + La forma en que obliga a implementar el código.
    + Cualquiera (sin ser autor del código) puede debuggear el sistema.

  + Por qué se eligió DOO (1')
    + Propiedades que se deseaban (45") (EN DUDA)
      + Modularidad, para encapsular conceptos abstractos de implementación en módulos sencillos de utilizar.
      + Reutilización, de componentes que puedan ser reusados en distintos módulos/sistemas.
      + Extensibilidad de funcionalidades mediante métodos que puedan ser acoplables.
      + Inversión del control, se explicita una orden y el sistema decide cómo atenderla.
  + Diagrama UML de las clases más importantes (15")
  + Perfiles de usuario (40")
  ````

 - Estructura **(1')**
  + Learninspy es un framework que sigue un DOO **(35")**
    + En el speech, solo mencionar breve las propiedades más importantes.
  + Perfiles de usuario **(25")**

 - Características (6')
  + Listar características **(1'30")**
    + Importancia en la flexibilidad (e.g. func de activ, optimizadores)
    + Anticipar demo
  + Explotación del cómputo distribuido (listar) **(30")**
  + Explicar esquema de entrenamiento distribuido (4'30")
    + Diagrama del esquema **(1'30")**
    + Funciones de consenso **(1')**
    + Criterios de corte **(30")**
    + Esquemas similares (1') ???????????????????????????
      + Convergencia... está dificil explicar eso...
      + Con dist belief se hizo el experimento de gatos?
      + Si no mencionás los otros esquemas, entonces quizás ni conviene dar la ventajas

- Demo rápida con ejemplo de uso **(5')**
  - Activación nueva **(1')**
  - Ejemplo **(4')**

#### Evaluación de desempeño: **(3')**

 + Testeo en integración continua **(1')**
  + Mencionar rápido qué es cada cosa.
  + Mostrar links? introduce riesgo.
    + Puede ser q muestre el slide 10" y luego sigo explicando en los links.

 + Materiales **(40")**
  - Recursos computacionales
  - Sólo mencionar bases de datos?

 + Mostrar resultados de cada experimento de validación **(1'30")**

#### Casos de aplicación : (7')
  + Introducción **(1')**
    - EEG **(30")**
      + No definir tanto EEG (ya está en pantalla)
      + Resaltar diferencia de técnicas
    - BCI **(30")**
      + Resaltar motivación de sillas para sujetos con esclerósis múltiple
  + P300 **(3')**
    - Conceptos **(1')**
    - Corpus y experimentos **(1')** NO PIERDAS TIEMPO EN EL CORPUS
      + Aclarar que es clasificación binaria!
    - Resultados **(1')**
      + Resaltar conclusiones!!

  + Habla imaginada (3')
    - Conceptos **(30")**
    - Corpus y experimentos (1'30")
      + Aclarar que es clasificación multiclase!
        + También se atacó un problema de regresión en la reducción de dimensiones.
      + Sólo menciona de donde se sacó
    - Resultados (1')
      + Resaltar conclusiones!!

 > No explicar tanto las metodologías usadas para la experimentación. Podrían mencionarse algunas particularidades que gracias a Learninspy se pudieron configurar.

#### Conclusiones: (2')
  - Corolarios **(50")**
    + Aclarar que los casos de aplicación eran de poca densidad, por lo que no relucen todos los aspectos del framework (e.g. entrenamiento distribuido)
    + Aprender tecnologías nuevas
      + Spark en mi laburo (evangelizador, tech leader)    
  - Gráfico de materias con analisis subjetivo **(40")**
  - Trabajos futuros **(30")**
  + Links (repo, docs)

  + Agradecimientos ?
