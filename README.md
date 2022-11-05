# ![imagen](https://user-images.githubusercontent.com/90228351/200121913-fa726792-68b2-4134-bacf-9166b837ba43.png)

Resolución de la evaluación práctica de ProContacto

## Ejercicio 2:

### 1. ¿Qué es un servidor HTTP?
Un servidor http es un software estandarizado que controla cómo los usuarios tienen acceso a los archivos contenidos en el servidor. Esta pieza de software es capaz de comprender URLs, para saber a qué archivo específico se quiere acceder, y el verbo, para comprender la acción que el cliente está solicitando.

### 2. ¿Qué son los verbos HTTP? Mencionar los más conocidos
Los verbos https son palabras en texto plano (legibles por humanos) que le indican al servidor el tipo de petición que el cliente está realizando. Los más conocidos son:

* `Get`: Se utiliza para consultar un recurso, estas peticiones solo recuperan datos, no realizan ningún cambio en el servidor.

* `Post`: Se utiliza para enviar contenido a un recurso en específico , esta petición causa un cambio de estado o efectos secundarios en el servidor

* `Put`: Causa una petición idéntica a post, pero el objetivo de put es modificar las representaciones actuales del recurso ya existentes con el contenido enviado

* `Delete`: Borra un recurso en específico

### 3. ¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers?
En un intercambio bajo el protocolo http, request y response son la base de todas las comunicaciones, el cliente realiza una **petición** (request) al servidor ( a través de, por ejemplo, un navegador web) , la cual el servidor recibe, interpreta, y trata de servir a través de una **respuesta** (response). Según el estándar de http, el cliente es el que realiza las peticiones, y el servidor es el que devuelve las respuestas, nunca al revés.

También existen los **headers**, que son la forma en el que el cliente y el servidor se pasan información adicional, tanto en una petición como en una respuesta. El header consiste en un `nombre` (que ignora mayúsculas y minúsculas) seguido de `:` y luego su `valor`.



