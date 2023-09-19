# Evaluacion Practica ProContacto
Este archivo esta hecho con el objetivo de aprender y mostrar mis conocimientos sobre Salesforce, resolviendo preguntas y problemas que el grupo ProContacto me presenta.

## Ejercicio 1
### Instalación de ambiente
1. Instalación de Visual Studio Code
   ![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/2255dd80-98fb-4735-82c3-90e2eebdd17b)
2. Instalación de GIT y GIT Bash
   
   ![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/bda86694-7fbe-4308-87ec-c0486147a71a)

## Ejercicio 2
Las siguientes preguntas están orientadas a la comprensión del protocolo HTTP. Son agnósticas al lenguaje de programación, la idea es comprender los conceptos del estándar:
1. **¿Qué es un servidor HTTP?:** Es un software que procesa las aplicaciones por el lado del servidor, brindando espacio y estructura a los sitios web para que almacenen y manejen sus paginas web. Del mismo modo, permite realizar conexiones bidireccionales o unidireccionales, sincronas o asincronas con el cliente para ceder o generar una respuesta.
2. **¿Qué son los verbos HTTP? Mencionar los más conocidos**: Los verbos HTTP son los metodos de solicitud utilizados para indicar una accion que desea realizar para un recurso determinado. De los verbos mas conocidos podemos encontrar los siguientes:
    * GET: Utilizado para obtener información de un recurso.
    * POST: Utilizado para crear o enviar datos.
    * PUT: Utilizado para actualizar un recurso existente.
    * DELETE: Utilizado para eliminar un recurso existente.
3. **¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers?:** Un request es una solicitud que un cliente envia a un servidor, por otro lado un response es una respuesta que un servidor le envia a un cliente. Por el lado de los headers, son campos que proporcionan información adicional sobre las solicitudes o respuestas HTTP.
4. **¿Qué es un queryString? (En el contexto de una url):** Un queryString es una cadena de caracteres que se agrega al final de la URL, el cual tiene como proposito dar información adicional sobre la solicitud que se haga. La queryString despues de la URL estara separada un por un signo de interrogación(?), siguiendo de este, se encontraran las pares clave-valor que nos daran las claves del nombres de la información con sus respectivos valores denotados despues del signo igual(=). El queryString cuenta con varios propositos como filtrar resultados, enviar parametros, entre otros.
5. **¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?:** Los responseCode es información de estado sobre una solicitud HTTP, indicando cual es la respuesta a esta solicitud. El responseCode hoy en dia tiene una gran variedad de codigos con distintos significados, sin embargo, aqui mostrare los principales responseCode los cuales son la base de los demas:
    * | Código | Estado |
      |---|---|
      | 1XX | Indica que una solicitud realizada al servidor sigue en curso, lo que necesariamente no es un error sino información extra. |
      | 2XX | Indica que el estado HTTP funciona perfectanente y no hay ninguna falla. |
      | 3XX | Indica el redireccionamiento a otros recursos, lo que muestra exactamente que un recurso a sido trasladado a una nueva ubicación. |
      | 4XX | Indica algun fallo en el navegador y/o en la solicitud, lo que indica a grandes rasgos, un error. |
      | 5XX | Indica un error que se presenta al extremo del servidor. |
6. **¿Cómo se envía la data en un GET y cómo en un POST?:** Los datos de un metodo GET se hacen a traves de la URL, donde despues de esta, se coloca un signo de interrogación y las pares clave-valor. Los datos de un metodo POST, por otro lado, se envia en el cuerpo de la solicitud lo que le permite enviar cualquier tipo de dato y comunmente se envia en una estructura JSON.
7. **¿Qué verbo http utiliza el navegador cuando accedemos a una página?:** El metodo GET, ya que como se ha mencionado antes, este verbo nos ayuda a obtener la información de un recurso, en este caso la pagina web.
8. **Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles:** JavaScript Object Notation(JSON) es un formato de datos legible basado en un subconjunto del lenguaje de programación JavaScript, el cual su sintaxis es similar a la de los diccionarios, con pares clave-valor separados por comas(,). Extensible Markup Language(XML) es un lenguaje marcado para representar datos estructurados con una sintaxis basada en el uso de etiquetas. A continuación se presentaran los ejemplos de cada una de las estructuras:
    * JSON
    ```json
    [
        {
            "nombre": "Perro",
            "tipo": "Mamífero",
            "alimentacion": "Carnivoro",
            "habitat": "Terrestre"
        },
        {
            "nombre": "Gato",
            "tipo": "Mamífero",
            "alimentacion": "Carnivoro",
            "habitat": "Terrestre"
        }
    ]
    ```
    * XML
    ```xml
    <animales>
        <animal>
            <nombre>Perro</nombre>
            <tipo>Mamífero</tipo>
            <alimentacion>Carnivoro</alimentacion>
            <habitat>Terrestre</habitat>
        </animal>
        <animal>
            <nombre>Gato</nombre>
            <tipo>Mamífero</tipo>
            <alimentacion>Carnivoro</alimentacion>
            <habitat>Terrestre</habitat>
        </animal>
    </animales>
    ```
9. **Explicar brevemente el estándar SOAP:** SOAP o tambien conocido como Simple Object Access Protocol, es un protocolo de mensajeria utilizada para el intercambio de datos entre aplicaciones web, en donde SOAP hace uso del lenguaje XML y el protocolo HTTP como protocolo de transporte. SOAP suele tener uso en servicios web, comunicación entre aplicaciones e integración de sistemas, lo que lo hace un estandar muy abierto a una amplia gama de aplicaciones.
10. **Explicar brevemente el estándar REST Full:** Los servicios REST o Representational State Transfer, es una base de principios de arquitectura utilizado para desarrollar y diseñar servicios web, utilizando HTTP y URI el cual se encarga de la identificación de recursos. Al igual que SOAP tiene una amplia gama de aplicaciones, sin embargo REST tiene una gran facilidad para entender y una buena eficiencia.
11. **¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?:** Como ya se ha mencionado anteriormente, son los pares clave-valor que se envian en la solicitud HTTP, donde estos proporcionan información adicional sobre tipo de contenido, tamaño de contenido o la autenticación del usuario. Por el lado del key Content-type en un header, este indicara el tipo de contenido que se esta enviando en el body del request, ya sea en HTTP, JSON, XML e incluso otros formatos.
