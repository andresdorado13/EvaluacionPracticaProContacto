# Evaluacion Practica ProContacto
Este archivo esta hecho con el objetivo de aprender y mostrar mis conocimientos sobre Salesforce, resolviendo preguntas y problemas que el grupo ProContacto me presenta.

* [Ejercicio 1](#ejercicio-1)
* [Ejercicio 2](#ejercicio-2)
* [Ejercicio 3](#ejercicio-3)
* [Ejercicio 4](#ejercicio-4)
* [Ejercicio 5](#ejercicio-5)
* [Ejercicio 6](#ejercicio-6)

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

## Ejercicio 3
1. Realizar un request GET a la URL: https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json
   ![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/41f52ecb-982f-410a-8fb8-3a62ada3dd4a)

2. Realizar un request POST a la URL anterior, y con body:
    ```json
        {
            "name":"Tu nombre",
            "email":"tunombre.tuapellido@procontacto.com.mx"
        }
    ```
    Tip: (Marcar la opción “raw” como body)
    ![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/aec594ff-4f36-4f3e-a1a9-a562fa486c8d)

3. Realizar nuevamente un request GET a la URL: https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json
   ![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/42a8d81f-23a1-4221-ab18-6e26d9e35892)

### ¿Qué diferencias se observan entre las llamadas el punto 1 y 3?
En el punto 1 al hacer el GET en la URL indicada, habian registros previos de contactos con nombres y correos de personas diferentes a mi, mientras que en el punto 3 al hacer la llamada aparecen los registros nuevamente con la diferencia de que aparecian mis datos registrados a partir del punto 2, donde realice un metodo POST.

# Ejercicio 4
Link para ver mi perfil con los cursos: https://www.salesforce.com/trailblazer/andresdorado

# Ejercicio 5

# Ejercicio 6
## Soluciones de Salesforce
1. **¿Qué es Salesforce?:** Es una plataforma de software de gestión de relaciones con el cliente (CRM) basada en la nube que ayuda a las empresas a conectar con sus clientes, comprender sus necesidades y venderles de manera más efectiva, ademas este ofrece una amplia gama de productos y servicios que se encuentran en las áreas de ventas, marketing, comercio y servicio al cliente.
2. **¿Qué es Sales Cloud?:** Es una plataforma de gestión CRM desarrollada por Salesforce y está diseñado específicamente para ayudar a las empresas a administrar y automatizar sus procesos de ventas y marketing, así como a mejorar la colaboración entre equipos de ventas y servicio al cliente.
3. **¿Qué es Service Cloud?:** Es una solución de servicio al cliente de Salesforce que ayuda a las empresas a brindar un servicio al cliente excepcional a través de múltiples canales, incluidos teléfono, correo electrónico, autoservicio, entre otros.
4. **¿Qué es Health Cloud?:** Es una solución de gestión de pacientes y CRM de atención médica basada en la nube que permite la colaboración entre proveedores de atención médica, pagadores y pacientes. Health Cloud ofrece una amplia gama de funciones para ayudar a las organizaciones de atención médica a mejorar la atención al paciente, la eficiencia y los resultados.
5. **¿Qué es Marketing Cloud?:** Es una plataforma de marketing digital basada en la nube que ayuda a las empresas a crear y ejecutar campañas de marketing efectivas a través de múltiples canales, incluidos correo electrónico, redes sociales, dispositivos móviles y publicidad digital.

## Funcionalidades de Salesforce
1. **¿Qué es un RecordType?:** Es una configuración que permite la personalización de la forma en que se recopilan y presentan los datos en un objeto personalizable. Los RecordTypes se usan para tanto objetos estandar como personalizados, los cuales tienen diferentes conjuntos de campos o procesos comerciales asociados.
2. **¿Qué es un ReportType?:** 
3. **¿Qué es un Page Layout?:** 
4. **¿Qué es un Compact Layout?:** 
5. **¿Qué es un Perfil?:** 
6. **¿Qué es un Rol?:** 
7. **¿Qué es un Validation Rule?:** 
8. **¿Qué diferencia hay entre una relación Master Detail y Lookup?:** 
9. **¿Qué es un Sandbox?:** 
10. **¿Qué es un ChangeSet?:** 
11. **¿Para qué sirve el import Wizard de Salesforce?:** 
12. **¿Para qué sirve la funcionalidad Web to Lead?:** 
13. **¿Para qué sirve la funcionalidad Web to Case?:** 
14. **¿Para qué sirve la funcionalidad Omnichannel?:** 
15. **¿Para qué sirve la funcionalidad Chatter?:** 

