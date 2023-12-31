# Evaluacion Practica ProContacto
Este archivo esta hecho con el objetivo de aprender y mostrar mis conocimientos sobre Salesforce, resolviendo preguntas y problemas que el grupo ProContacto me presenta.

* [Ejercicio 1](#ejercicio-1)
* [Ejercicio 2](#ejercicio-2)
* [Ejercicio 3](#ejercicio-3)
* [Ejercicio 4](#ejercicio-4)
* [Ejercicio 5](#ejercicio-5)
* [Ejercicio 6](#ejercicio-6)
* [Ejercicio 7](#ejercicio-7)
* [Ejercicio 8](#ejercicio-8)

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
Datos almacenados de forma estándar y como se relacionan los objetos en Salesforce:
1. **Lead (Cliente potencial):**
   * Es un cliente potencial que demostró interés en un producto o servicio ofrecido por la marca por medio de la interacción con contenidos y otros materiales.
   * Los leads puede convertirse en contactos, cuentas y oportunidades una vez se hayan establecido un interés genuino.
2. **Account (Cuenta):**
   * Es una cuenta individual, que es una organización o persona involucrada con su negocio (como clientes, competidores y socios).
   * Una cuenta puede tener muchas oportunidades, contactos, cuentas, casos y activos.
3. **Contact (Contacto):**
   * Representa a una persona individual con la que la empresa tiene una relación, generalmente asociada a una cuenta.
   * Un contacto solo tiene una cuenta y tiene muchos contactos, casos y activos.
4. **Opportunity (Oportunidad):**
   * Es una venta potencial o una transacción en curso con un cliente o una cuenta.
   * Una oportunidad tiene una cuenta y un libro de precios, pero tiene muchas cotizaciones.
5. **Product (Producto):**
   * Es un artículo o servicio que la empresa vende.
   * Un producto puede tener muchos productos, casos, activos y cotizaciones.
6. **PriceBook (Catálogo de precios):**
   * Un conjunto de precios para productos específicos en diferentes situaciones o mercados.
   * Un catálogo de precios puede tener muchas oportunidades.
7. **Quote (Cotización):**
   * Una propuesta de precios para productos o servicios que se ofrece a un cliente.
   * Las cotizaciones están relacionadas con una oportunidad y muchos productos.
8. **Asset (Activo):**
   * Un producto o servicio que un cliente ha adquirido y está siendo utilizado.
   * Un activo puede tener solo un contacto, cuenta y producto, aunque puede tener muchos casos relacionados.
9. **Case (Caso):**
   * Representa una solicitud, problema o consulta de un cliente que necesita ser gestionado.
   * Un caso solo tiene un contacto, cuenta, activo y producto relacionado, pero puede tener muchos casos y artículos.
10. **Article (Artículo):**
   * Es información útil o documentos que pueden ser utilizados para el soporte al cliente.
   * Los artículos a menudo se utilizan en la resolución de muchos casos para proporcionar información a los clientes.
## Diagrama de relaciones
![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/03aed5f3-13a4-45ac-8d5d-9206af157d66)

# Ejercicio 6
## Soluciones de Salesforce
1. **¿Qué es Salesforce?:** Es una plataforma de software de gestión de relaciones con el cliente (CRM) basada en la nube que ayuda a las empresas a conectar con sus clientes, comprender sus necesidades y venderles de manera más efectiva, ademas este ofrece una amplia gama de productos y servicios que se encuentran en las áreas de ventas, marketing, comercio y servicio al cliente.
2. **¿Qué es Sales Cloud?:** Es una plataforma de gestión CRM desarrollada por Salesforce y está diseñado específicamente para ayudar a las empresas a administrar y automatizar sus procesos de ventas y marketing, así como a mejorar la colaboración entre equipos de ventas y servicio al cliente.
3. **¿Qué es Service Cloud?:** Es una solución de servicio al cliente de Salesforce que ayuda a las empresas a brindar un servicio al cliente excepcional a través de múltiples canales, incluidos teléfono, correo electrónico, autoservicio, entre otros.
4. **¿Qué es Health Cloud?:** Es una solución de gestión de pacientes y CRM de atención médica basada en la nube que permite la colaboración entre proveedores de atención médica, pagadores y pacientes. Health Cloud ofrece una amplia gama de funciones para ayudar a las organizaciones de atención médica a mejorar la atención al paciente, la eficiencia y los resultados.
5. **¿Qué es Marketing Cloud?:** Es una plataforma de marketing digital basada en la nube que ayuda a las empresas a crear y ejecutar campañas de marketing efectivas a través de múltiples canales, incluidos correo electrónico, redes sociales, dispositivos móviles y publicidad digital.

## Funcionalidades de Salesforce
1. **¿Qué es un RecordType?:** Es una configuración que permite la personalización de la forma en que se recopilan y presentan los datos en un objeto personalizable. Los RecordTypes se usan para tanto objetos estandar como personalizados, los cuales tienen diferentes conjuntos de campos o procesos comerciales asociados.
2. **¿Qué es un ReportType?:** Un Report Type determina qué objetos y relaciones están disponibles para su uso en un informe (son herramientas que permiten a los usuarios analizar y visualizar datos de sus objetos estándar y personalizados). Cuando se crea un informe, se debe seleccionar un Report Type para establecer qué datos puedes incluir en ese informe.
3. **¿Qué es un Page Layout?:** Es una configuración que define la apariencia y la disposición de los campos y secciones en la interfaz de usuario de un registro de un objeto.
4. **¿Qué es un Compact Layout?:** Es una configuración que define qué campos y etiquetas se muestran de manera resumida en la parte superior de un registro en la vista de lista, la vista de detalles y en la tarjeta de resumen. 
5. **¿Qué es un Perfil?:** Es una configuración que asigna las capacidades y el acceso a datos que un usuario o grupo de usuarios tiene dentro de la plataforma. Los perfiles son una parte esencial del modelo de seguridad y acceso de Salesforce y se utilizan para controlar quién puede ver, editar, eliminar o compartir registros y qué acciones pueden realizar en la plataforma.
6. **¿Qué es un Rol?:** Es una entidad que se utiliza para definir la jerarquía de acceso y la estructura organizativa dentro de una organización.
7. **¿Qué es un Validation Rule?:** Es una regla lógica de validación que se utiliza para garantizar que los datos ingresados en los registros cumplan con ciertos criterios específicos antes de que se puedan guardar o actualizar.
8. **¿Qué diferencia hay entre una relación Master Detail y Lookup?:** La principal diferencia entre una relación Master-Detail y Lookup en Salesforce radica en la dependencia y el control. Una relación Master-Detail crea una fuerte dependencia entre los registros de detalle y maestro, mientras que una relación Lookup es más flexible y permite que los registros de detalle existan de forma independiente. 
9. **¿Qué es un Sandbox?:** Es un entorno aislado y seguro que permite a las organizaciones desarrollar, probar y realizar cambios en sus aplicaciones y configuraciones de Salesforce sin afectar al entorno de producción en vivo.
10. **¿Qué es un ChangeSet?:** Es una herramienta de Salesforce que se utiliza para gestionar y mover metadatos entre diferentes entornos de Salesforce, como sandbox y producción, o entre diferentes organizaciones Salesforce.
11. **¿Para qué sirve el import Wizard de Salesforce?:** Es una herramienta que facilita la importación de datos desde fuentes externas a tu organización de Salesforce. Esta se usa para migrar datos desde otras aplicaciones, hojas de cálculo de Excel u otras fuentes de datos a la instancia de Salesforce.
12. **¿Para qué sirve la funcionalidad Web to Lead?:** Es una característica que permite a las organizaciones capturar automáticamente la información de contacto de los visitantes de su sitio web y convertirla en registros de "Lead" (visitantes como posibles clientes) en su instancia de Salesforce. 
13. **¿Para qué sirve la funcionalidad Web to Case?:** Es una característica que permite a las organizaciones capturar automáticamente las solicitudes de soporte o casos de los clientes y visitantes de su sitio web y convertirlas en registros de "Case" (caso o solicitud de soporte) en su instancia de Salesforce. 
14. **¿Para qué sirve la funcionalidad Omnichannel?:** Se utiliza para mejorar y optimizar la gestión de interacciones y casos de servicio al cliente en múltiples canales, lo que permite brindar una experiencia de atención al cliente más fluida y consistente.
15. **¿Para qué sirve la funcionalidad Chatter?:** Chatter funciona como una herramienta de colaboración y comunicación social que sirve para mejorar la comunicación y la interacción entre los usuarios en una organización.

## Conceptos generales
1. **¿Qué significa SaaS?:** El significado de SaaS es Software as a Service, un modelo de distribución de software en el que el software se proporciona a los usuarios a través de Internet como un servicio en lugar de requerir que lo instalen y lo ejecuten en sus propios dispositivos o servidores locales.
2. **¿Salesforce es Saas?:** Salesforce si es SaaS, debido a que los usuarios pueden acceder a su plataforma y aplicaciones a través de Internet mediante una suscripción. Salesforce gestiona toda la infraestructura subyacente, incluido el almacenamiento de datos, la seguridad y las actualizaciones de software, en donde los usuarios pueden utilizarlo para realizar actividades relacionadas con la gestión de clientes, como la administración de contactos, el seguimiento de ventas, la gestión de campañas de marketing y la atención al cliente, todo ello desde la comodidad de una interfaz basada en la web o a través de aplicaciones móviles.
3. **¿Qué significa que una solución sea Cloud?:** Significa que no requiere de instalar ni mantener maquinas propias para el software, sino por otro lado, el software o servicio se encuentra en servidores remotos y se puede acceder a estos a traves de internet en vez de instalar.
4. **¿Qué significa que una solución sea On-Premise?:** Da lugar a que el software o servicio se instala y ejecuta en servidores locales o en la infraestructura de la empresa, en lugar de ejecutarse en servidores remotos en la nube. 
5. **¿Qué es un pipeline de ventas?:** Es una representación visual o conceptual del proceso que sigue una empresa para adquirir nuevos clientes y convertirlos en ventas, proporcionando formas de rastrear y gestionar oportunidades de ventas.
6. **¿Qué es un funnel de ventas?:** Tiene un concepto parecido a pipeline de ventas, pero se enfoca más en el proceso de adquirir y convertir clientes potenciales en clientes reales a medida que avanzan a través de varias etapas. 
7. **¿Qué significa Customer Experience?:** Es la percepción general que tiene un cliente sobre todas las interacciones y puntos de contacto que tiene con una empresa a lo largo de su ciclo de vida como cliente.
8. **¿Qué significa omnicanalidad?:** Es un enfoque estratégico en el ámbito del marketing y la atención al cliente que se centra en proporcionar una experiencia consistente y unificada a los clientes a través de múltiples canales de comunicación y puntos de contacto. 
9. **¿Qué significa que un negocio sea B2B?¿Qué significa que un negocio sea B2C?¿Qué es un KPI?:**
   * B2B significa Business to Business, lo que se refiere a las transacciones comerciales y relaciones entre las empresas.
   * B2C significa Business to Consumer, lo que se refiere a las transacciones comerciales entre una empresa y sus consumidores individuales.
   * KPI significa Key Performance Indicator, la cual es una métrica utilizada para medir y evaluar el desempeño de una empresa, un proyecto o un proceso.
10. **¿Qué es una API y en qué se diferencia de una Rest API?:** Una API es un conjunto de reglas y protocolos que permiten que diferentes aplicaciones o componentes de software se comuniquen entre sí. Las APIs definen cómo los programas pueden solicitar y compartir datos y funcionalidades. Por otro lado las Rest APIs son un tipo especifico de APIs que siguen un conjunto de principios y protocolos particulares para facilitar la comunicación de aplicaciones web a traves de HTTP.
11. **¿Qué es un Proceso Batch?:** Es un procesamiento de datos en la que un conjunto de tareas o trabajos se agrupan y se ejecutan en lotes predefinidos en lugar de procesarse de forma individual y en tiempo real. 
12. **¿Qué es Kanban?:** Es una metodología de gestión que se utiliza para optimizar el flujo de trabajo y la eficiencia de procesos.
13. **¿Qué es un ERP?:** ERP significa Enterprise Resource Planning, lo que se refiere a un sistema de planificación de recursos empresariales que integra y administra una variedad de procesos y funciones comerciales clave en una organización.
14. **¿Salesforce es un ERP?:** No, ya que un ERP se ocupa de una amplia variedad de procesos empresariales, incluyendo la gestión financiera, la gestión de recursos humanos, la gestión de inventarios y cadenas de suministro, la producción y más. En cambio, Salesforce se especializa en la gestión de las interacciones con los clientes(CRM) y la gestión de ventas.

# Ejercicio 7
1. Consultar tu ID haciendo un GET con POSTMAN a este WS: https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json
![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/c96a964e-a253-439e-9862-f2573993772a)
2. Agregar un campo al objeto Contact llamado idprocontacto de tipo texto de 255 caracteres. De la siguiente manera:
![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/6f6da0d5-798c-4503-b8c8-f0d4cbcdd764)
**No omitir poner el siguiente check cuando se crea el campo.**
![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/01019685-e31f-4269-adc6-2d580e0d703a)
**Evidencia del campo idprocontacto creado**
![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/73692162-a08d-4144-9491-53ec0ca47cf8)

4. Desarrollar un trigger para que cuando un usuario Modifica o Crea un contacto de Salesforce completando el campo generado el punto B con TU id obtenido en el punto A, se invoque al Web Service con el idprocontacto obtenga los datos de email de la respuesta y actualice el campo email del contacto. Usar Playground 1.
   * Primero cree el trigger UpdateContactEmailTrigger en el objeto Contacto para despues de insertar y actualizar, el cual se verificara si el campo idprocontacto__c tiene un valor nulo o en blanco y más adelante se invoca el servicio web de manera asincrónica solo en el evento after insert.
   ```apex
   trigger UpdateContactEmailTrigger on Contact (after insert, after update) {
      List<Id> contactIds = new List<Id>();
      for (Contact contact : Trigger.new) {
         if (String.isNotBlank(contact.idprocontacto__c)) {
            contactIds.add(contact.Id);
         }
      }
      if (!contactIds.isEmpty()) {
         if (Trigger.isAfter && Trigger.isInsert) {
            ContactWebService.updateContactEmail(contactIds);
         }
      }
   }
    ```
   * Luego del trigger, hice la creación de una clase web service con el nombre de ContactWebService, el cual hacemos la construcción de la URL del servicio web utilizando el campo idprocontacto__c, realizo la llamada al servicio web utilizando HTTPRequest, luego creo un objeto HTTP para enviar la solicitud, procesamos la respuesta y analizamos la respuesta JSON para obtener el email y actualizamos el campo de email del contacto.
   ```apex
     public class ContactWebService {
        @future(callout=true)
        public static void updateContactEmail(List<Id> contactIds) {
           List<Contact> contactsToUpdate = new List<Contact>();
              for (Id contactId : contactIds) {
                 Contact contact = [SELECT idprocontacto__c FROM Contact WHERE Id = :contactId AND idprocontacto__c != null LIMIT 1];
                 if (contact != null && String.isNotBlank(contact.idprocontacto__c)) {
                    String serviceURL = 'https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts/' + contact.idprocontacto__c + '.json';
                    HttpRequest request = new HttpRequest();
                    request.setEndpoint(serviceURL);
                    request.setMethod('GET');
                    request.setHeader('Content-Type', 'application/json');
                    Http http = new Http();
                    HttpResponse response = http.send(request);
                    if (response.getStatusCode() == 200) {
                       Map<String, Object> jsonResponse = (Map<String, Object>) JSON.deserializeUntyped(response.getBody());
                       String email = (String) jsonResponse.get('email');
                       contact.Email = email;
                       contactsToUpdate.add(contact);
                    }
                 }
              }
              if (!contactsToUpdate.isEmpty()) {
                 update contactsToUpdate;
              }
          }
      }
    ```
   * Creo un contacto con mi nombre y mi ID obtenido en el punto 1, el cual es '-Nej2RiB0mG0TCDmss8_' (el campo correo queda vacio).
![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/a682821a-b277-4884-90a2-ed3e24615252)
   * Al momento de crear el contacto, se confirma la creación de este y se evidencia la agregación del correo respectivamente.
![image](https://github.com/andresdorado13/EvaluacionPracticaProContacto/assets/64713965/deaf2d9f-b78a-4661-b888-1db04205a86b)

# Ejercicio 8
Corrección del ejercicio 7
## Trigger
```apex
trigger UpdateContactEmailTrigger on Contact (after insert, after update) {
   List<Id> contactIds = new List<Id>();
   for (Contact contact : Trigger.new) {
      if (String.isNotBlank(contact.idprocontacto__c)) {
         contactIds.add(contact.Id);
      }
   }
   if (!contactIds.isEmpty()) {
      if ((Trigger.isAfter && Trigger.isInsert) || (Trigger.isAfter && Trigger.isUpdate)) {
         ContactWebService.updateContactEmail(contactIds);
      }
   }
}
```

## Web service
```apex
public class ContactWebService {
   @future(callout=true)
   public static void updateContactEmail(List<Id> contactIds) {
      List<Contact> contactsToUpdate = [SELECT idprocontacto__c FROM Contact where Id IN : contactIds AND idprocontacto__c!=null];
      for (Integer i=0 ; i<contactsToUpdate.size() ; i++) {
         String serviceURL = 'https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts/' + contactsToUpdate[i].idprocontacto__c + '.json';
         HttpRequest request = new HttpRequest();
         request.setEndpoint(serviceURL);
         request.setMethod('GET');
         request.setHeader('Content-Type', 'application/json');
         Http http = new Http();
         HttpResponse response = http.send(request);
         if (response.getStatusCode() == 200) {
            Map<String, Object> jsonResponse = (Map<String, Object>) JSON.deserializeUntyped(response.getBody());
            String email = (String) jsonResponse.get('email');
            contactsToUpdate[i].Email = email;
         }
      }
      update contactsToUpdate[i];
   }
}
```
