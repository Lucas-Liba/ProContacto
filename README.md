# ![imagen](https://user-images.githubusercontent.com/90228351/200121913-fa726792-68b2-4134-bacf-9166b837ba43.png)

Resolución de la evaluación práctica de ProContacto

## Ejercicio 2:



1.	Un servidor http es un software estandarizado que controla cómo los usuarios tienen acceso a los archivos contenidos en el servidor. Esta pieza de software es capaz de comprender URLs, para saber a qué archivo específico se quiere acceder, y el verbo, para comprender la acción que el cliente está solicitando.

2.	Los verbos https son palabras en texto plano (legibles por humanos) que le indican al servidor el tipo de petición que el cliente está realizando. Los más conocidos son:
•	Get: Se utiliza para consultar un recurso, estas peticiones solo recuperan datos, no realizan ningún cambio en el servidor.
•	Post: Se utiliza para enviar contenido a un recurso en específico, esta petición causa un cambio de estado o efectos secundarios en el servido
•	Put: Causa una petición idéntica a post, pero el objetivo de put es modificar las representaciones actuales del recurso ya existentes con el contenido enviado
•	Delete: Borra un recurso en específico

3.	En un intercambio bajo el protocolo http, request y response son la base de todas las comunicaciones, el cliente realiza una petición (request) al servidor (a través de, por ejemplo, un navegador web) , la cual el servidor recibe, interpreta, y trata de servir a través de una respuesta (response). Según el estándar de http, el cliente es el que realiza las peticiones, y el servidor es el que devuelve las respuestas, nunca al revés.
También existen los headers, que son la forma en el que el cliente y el servidor se pasan información adicional, tanto en una petición como en una respuesta. El header consiste en un nombre (que ignora mayúsculas y minúsculas) seguido de : y luego su valor.

4.	En el contexto de una URL, un query String es la forma que tiene el usuario de realizar peticiones adicionales en una URL. Está precedido por un signo de pregunta (?) y tiene el siguiente formato: nombre del parámetro, signo igual (=) , valor.

5.	El response code es el código de estado de respuesta de http. Los posibles valores devueltos tienen los siguientes significados
•	1xx: Son repuestas afirmativas, indica que el servidor recibe la respuesta y la está procesando

•	2xx: Son respuestas satisfactorias, indica que la petición fue procesada correctamente

•	3xx: Informan redirecciones, indica que el cliente necesita realizar más acciones para finalizar la petición

•	4xx: Informan un error del lado del cliente,  indica que hubo un error al procesar la petición a causa de un error del cliente

•	5xx: Informan un error del lado del servidor, indica que hubo un error al procesar una petición aparentemente valida

6.	En el caso de GET, la data que se envía de parte del usuario contendrá la URL a la que el usuario quiere acceder, ejemplo GET /index.html HTTP/1.1. Aunque existe la posibilidad, no es seguro enviar datos a través del método GET, ya que los datos enviados se enviarán a través de la URL, y serán visibles

7.	En el caso de POST, La manera más básica es incluir la palabra POST seguida de un URL y una tupla de palabras clave y valores, separados entre sí por un ampersand (&) POST /test HTTP/1.1field1=value1 & field2=value2. Aquí los datos se envían de forma oculta, es decir, el usuario no verá sus datos en la URL del sitio.

8.	Cuando accedemos a una página web, el navegador utiliza el verbo GET.

9.	JSON y XML son formatos de datos estructurados comúnmente utilizados para la transferencia de datos en la web. La gran diferencia entre estos dos es su sintaxis.
JSON significa JavaScript Object Notation, y nos remite a como JavaScript estructura sus objetos, con pares ordenados de palabras clave y valores, separados por ,.
un ejemplo de esta estructura es:
```json
{
  "departamento":8,
  "nombredepto":"Ventas",
  "director": "Juan Rodríguez",
  "empleados":[
    {
      "nombre":"Pedro",
      "apellido":"Fernández"
    },{
      "nombre":"Jacinto",
      "apellido":"Benavente"
    } 
  ]
}
```
XML por otro lado significa Extensive Markup Language (Lenguaje de marcado extensible), este formato nos remite un poco al formato HTML, con sus valores encerrados entre llaves, en el formato <palabra_clave>Valor</palabra_clave>, un ejemplo de esta estructura de datos es:.
```XML
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE Edit_Mensaje SYSTEM "Edit_Mensaje.dtd">

<Edit_Mensaje>
     <Mensaje>
          <Remitente>
               <Nombre>Nombre del remitente</Nombre>
               <Mail> Correo del remitente </Mail>
          </Remitente>
          <Destinatario>
               <Nombre>Nombre del destinatario</Nombre>
               <Mail>Correo del destinatario</Mail>
          </Destinatario>
          <Texto>
               <Asunto>
                    Este es mi documento con una estructura muy sencilla 
                    no contiene atributos ni entidades...
               </Asunto>
               <Parrafo>
                    Este es mi documento con una estructura muy sencilla 
                    no contiene atributos ni entidades...
               </Parrafo>
          </Texto>
     </Mensaje>
</Edit_Mensaje>
```
10.	SOAP significa (simple object access protocol) y como su nombre lo dice, es un protocolo que impone reglas sobre cómo dos procesos pueden comunicarse a través del intercambio de mediante XML,
•	El sobre, que define el contenido del mensaje y cómo va a procesarse
•	Un conjunto de reglas de codificación
•	Una convención para la llamada a procedimientos y respuestas


11.	REST es el acrónimo de REpresentational State Transfer,  aquí principalmente hablamos de una arquitectura, no de un estándar, aunque en la actualidad utiliza el término para hablar de cualquier interfaz que use directamente el protocolo http (puede utilizar cualquier protocolo, pero http es el más extendido) para obtener datos o indicar la ejecución de operaciones sobre los datos, en cualquier formato, sin ser necesario pasar por las abstracciones de los estándares como por ejemplo SOAP.

12.	En un request, los headers son información adicional que se envía junto con la petición o la respuesta, consiste consiste en un nombre (que ignora mayúsculas y minúsculas) seguido de: y luego su valor.
El Key Content-Type en el contexto de un header le dice al navegador el tipo de archivo que se espera como respuesta a esa petición.




## Ejercicio 3
Get Request:

![image3](https://user-images.githubusercontent.com/90228351/204668145-567d2ecd-ae0f-4133-ba21-cbe021f4d8e1.png)

Post Request:

![image1](https://user-images.githubusercontent.com/90228351/204668180-e9ac300e-4b0a-497a-966b-7aeab9854a5a.png)

Get Request, en la que ahora figura nuestro nombre:

![image2](https://user-images.githubusercontent.com/90228351/204668230-cccdb8f8-5350-4913-9313-d729db848dc5.png)

La diferencia entre estas dos llamadas es que luego de realizar un post request a la URL otorgada con nuestro nombre, apellido y correo,esa informacion ha quedado almacenada en el servidor, Por lo que al realizar una nueva get request, podemos ver que ahora nuestro nombre y correo esta listado en la informacion, en la primera request no estaba ahí.

## Ejercicio 4
Resolución de lo módulos aquí:
https://trailblazer.me/id/llibanotte

## Ejercicio 5

*Lead se le llama a un prospecto de venta que expreso interés en tu producto o compañía, El objeto lead representa uno de estos prospectos
*Account se le llama a la cuenta institución empresa o consumidor que queremos seguir, ya sea un cliente, un socio, o un competidor. El objeto account representa una cuenta individual, involucrada con el negocio
*Contact se le llama a los individuos asociados con tu cuenta, este objeto representa un contacto
*Opportunity se le llama al seguimiento de las ventas o negocios pendientes, este objeto representa una de esas “oportunidades”
*Product representa un objeto que la compañía vende
*PriceBook representa la lista de productos que la organización vende
*Quote representa un registro de los presupuestos hechos por productos y servicios, pueden crearse desde opportunity y enviarse como PDF por mail a los clientes
*Asset Es un modelo específico de producto que el cliente posee, puede representar tanto tus productos propios que el cliente usa o los productos de tu competidor que el cliente usa
*Case representa una descripción detallada de la devolución, problema o pregunta de un cliente. Se usa para mantener constancia y resolver los problemas de tu cliente
*Article Captura información sobre los productos y servicios de tu compañia, los cuales quieres tener disponibles en tu base de conocimientos

Estos objetos, ademas de tener funcionalidades en si mismas, tienen relaciones con otros objetos de Salesforce, detalladas en el siguiente diagrama UML:
![Diagrama de relaciones ](https://user-images.githubusercontent.com/90228351/201262166-b8b533a7-22e4-4608-a68a-3464aa12ce55.jpg)

## Ejercicio 6
### Soluciones Salesforce

A.	Salesforce es una solución de gestión para relaciones entre empresas y clientes basada en CRM.

B.	Sales Cloud es una herramienta de ventas todo en uno y CRM que combina todas las características que comúnmente encontrarías por separado en otras herramientas. Y sobre todo ello agrega la posibilidad de acceder desde cualquier lugar donde se tenga un dispositivo conectado a internet.

C.	Service Cloud es un servicio de atención al cliente que crea procesos de automatización basados en IA para proporcionar un servicio personalizado.

D.	Health Cloud es un sistema CRM focalizado en proporcionar servicios de atención médica que permiten una mejor interacción con los pacientes desde cualquier dispositivo.

E.	Marketing Cloud es un servicio que proporciona diversas herramientas para mejorar la interacción de las empresas con sus clientes actuales y potenciales, a través de todo tipo de canales.

### Funcionalidades de Salesforce


A.	Un Record Type es un objeto que ofrece diferentes registros de procesos de negocios y subvalores de listas de selección específicos para cada perfil de usuario

B.	Un ReportType define el grupo de registros y campos disponibles para un reporte basado en la relación entre el objeto primario y sus objetos relacionados. Los reportes solo mostraran los registros que cumplen con el criterio establecido en el ReportType

C.	Un Page Layout es la forma en la que el contenido está organizado; botones, links, campos, y listas relacionadas a objetos, todo esto puede personalizarse a conveniencia del usuario.

D.	Los Compact Layout están orientados a la vista móvil, permite mostrar rápidamente los registros clave tanto en la aplicación de Salesforce, como en Lightning Experience y en las integraciones de Outlook y Gmail

E.	Un perfil es lo que define cómo los usuarios acceden a los objetos y datos y que pueden hacer en la aplicación.

F.	El rol es la función de usuario o jerarquía que tiene cada usuario de una organización, se usa para determinar el nivel de acceso a los datos.

G.	Una Validation Rule se encarga de verificar que los datos que un usuario escribe en un registro concuerden con los estándares  especificados antes de que el usuario pueda guardar el registro

H.	La diferencia entre estos dos es que en Master Detail los objetos relacionados no son independientes entre sí, el determinado como Detail siempre permanecerá atado al Master, si este último desaparece, Detail desaparece también. En Lookup, los dos objetos permanecen independientes.

I.	Un sandbox es una funcionalidad que permite copiar la plataforma de Salesforce de tu empresa en un entorno separado. El objetivo es probar cambios o integraciones que se deseen hacer, para verificar que no causen ningún problema, también se pueden usar para capacitar empleados para usar la plataforma, ya que los cambios realizados aquí no afectarán a la plataforma original 

J.	ChangeSet se le llama a un conjunto de cambios que se pueden enviar de una organización de Salesforce a otras. Se pueden usar, por ejemplo, para llevar los datos testeados en un Sandbox a la organización original

K.	El Import Wizard de Salesforce es la manera más fácil de importar data hacia muchos de los objetos estándar de Salesforce, e incluso a objetos personalización. Esta herramienta permite importar hasta 50,000 registros a la vez.

L.	Salesforce Web-to-lead se basa en crear un sitio web orientado a capturar la información de un visitante y almacenarla como una nueva Lead en Salesforce

M.	Web-to-Case es una funcionalidad innovadora de Salesforce que tiene el objetivo de ayudar a reunir los pedidos de soporte de los clientes directamente desde el sitio web de la compañía con el objetivo de generar nuevos casos y acelerar la velocidad de respuesta

N.	Omnichannel es una funcionalidad altamente personalizable y declarativa (se configura sin necesidad de escribir código) que permite enrutar los diferentes tipos de elementos de trabajo hacia los agentes correspondientes 

O.	Chatter es una funcionalidad que permite la colaboración en tiempo real para que los usuarios puedan trabajar juntos.

### Conceptos Generales

A.	SaaS significa “Software as a Service”, es decir, software como un servicio. Es una forma de poner a disposición soluciones de tecnología por medio de la internet.


B.	Si, Salesforce es SaaS

C.	Que una solución sea cloud significa que el software no está instalado en computadoras internas de la empresa, sino que está en un servidor externo al que la empresa accede mediante internet

D.	Que una solución sea On-Premise significa que el software está instalado directamente en la computadora del cliente y accede a él localmente, sin necesidad de acceso a internet

E.	Un pipeline de ventas es una herramienta que tiene como objetivo apoyar al equipo de ventas en todas las etapas de la relación con el cliente, incluso antes de que se convierta en cliente

F.	Un funnel o embudo de ventas representa todo el proceso de cierre de un negocio, desde el momento de la captación hasta la conversión final. Aquí las oportunidades potenciales de venta se cualifican y se seleccionan para convertirlas en oportunidades reales.

G.	Customer experience se refiere a la experiencia del cliente, desde la primera interacción hasta la última

H.	Omnicanalidad significa integrar los distintos canales de comunicación en un único sistema con el fin de generar una atención más fluida con el cliente 


I.	B2B significa “Business to Business”, es decir negocio a negocio, y se refiere a las operaciones comerciales directas entre empresas. En cambio, B2C significa “Business to Consumer”, ósea negocio al consumidor, donde el foco de atención esta puesto en atender al cliente final
KPI significa “Key Performance Indicators” o “Indicadores Clave de Rendimiento” y son herramientas gráficas que sirven para medir el desempeño real frente a las expectativas.

J.	Una API (Application Programming Interface) Establece la conexión entre dos computadoras o softwares para que puedan enviarse datos. La diferencia principal con una Rest API es que las API se comunican con el formato aplicación-aplicación, mientras que una Rest API sigue el concepto de cliente y servidor.

K.	Un proceso Batch es un proceso que no requiere supervisión o control directo del usuario. Generalmente se utiliza en tareas repetitivas sobre grandes conjuntos de información.

L.	Kanban es una metodología de organización de trabajo basada en un tablero organizado por columnas, donde el tablero más básico puede representar“Trabajo pendiente”, “En progreso” , y “Terminado”. Las tareas individuales avanzan representadas por tarjetas a través del tablero hasta ser finalizadas


M.	Un ERP (Enterprise Resource Planning) es un sistema especializado que permite la unificación y organización de todas las áreas, con el objetivo de llevar la trazabilidad de todos los procesos, facilitando la planificación y la optimización de recursos

N.	No, Salesforce no es un ERP



