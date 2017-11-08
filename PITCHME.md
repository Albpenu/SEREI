theme : moon
---?image=http://img00.deviantart.net/eb3d/i/2012/268/c/6/http_blue_background_by_soulart2012-d5fu5n2.jpg
# Hypertext  Transfer Protocol
Protocolo de intercambios de informacion <br>cliente (Web)-servidor (HTTP)
---

### Características del HTTP
<ul>
<li style="font-size: 25px;"><b><u>Es sencillo</u></b>. Está pensado y desarrollado para ser leído y fácilmente interpretado por las personas, haciendo más facil la depuración de errores, y reduciendo la curva de aprendizaje para los que empiezan a trabajar con él.</li>
<li style="font-size: 25px;"><b><u>Es extensible</u></b>. Las cabeceras de HTTP, han hecho que este protocolo sea fácil de ampliar y de experimentar con él.</li>
<li style="font-size: 25px;"><b><u>Es un protocolo con sesiones, pero sin estados</u></b> (no guarda ningún dato entre dos peticiones en la mísma sesión); el uso de HTTP cookies sí lo permite.</li>
<li style="font-size: 25px;"><b><u>Se apoya en el uso del protocolo TCP</u></b>, que está orientado a conexión, aunque una conexión continua entre los participantes en la comunicación no es necesaria siempre. La versión del protocolo HTTP/2 usa multiplexación de mensajes sobre un única conexión, siendo así una comunicación más eficiente.</li>
</ul>
---

### Típica Sesión HTTP
<p style="font-size: 30px; text-align: left;">En protocolos cliente-servidor, como HTTP, las sesiones consisten en <b><u>3 fases:</u></b></p>
<ol>
<li style="font-size: 30px;">El cliente establece una <b><u>conexión TCP</u></b> (o la conexión apropiada si la capa de transporte no es TCP).</li>
<li style="font-size: 30px;">El cliente envía la <b><u>solicitud</u></b>, y espera la respuesta.</li>
<li style="font-size: 30px;">El servidor procesa la solicitud, enviando de vuelta la <b><u>respuesta</u></b>, proporcionando un código de estado y datos adecuados.</li>
</ol>
---

### Cabeceras HTTP
<p style="font-size: 25px; text-align: left;">Las cabeceras de mensaje HTTP se usan para describir un recurso, o el comportamiento del servidor o del cliente. Permiten que el cliente y el servidor pasen información adicional con la solicitud o la respuesta.<br> Un encabezado de solicitud consiste en su nombre insensible a mayúsculas y minúsculas seguido de dos puntos ':', luego por su valor (sin saltos de línea). Un espacio en blanco antes de que se ignore el valor.</p>

---
#### Las cabeceras pueden ser agrupados de acuerdo a sus contextos:
<ul>
<li style="font-size: 25px;"><b><u>Encabezado general</u></b>. Encabezados que se aplican tanto a las solicitudes como a las respuestas, pero que no guardan relación con los datos transmitidos en el cuerpo.</li>
<li style="font-size: 25px;"><b><u>Encabezado de solicitud</u></b>. Encabezados que contienen más información sobre el recurso que se va a buscar o sobre el propio cliente.</li>
<li style="font-size: 25px;"><b><u>Encabezado de respuesta</u></b>. Encabezados con información adicional sobre la respuesta, como su ubicación o sobre el servidor en sí (nombre y versión, etc.).</li>
<li style="font-size: 25px;"><b><u>Encabezado de entidad</u></b>. Encabezados que contienen más información sobre el cuerpo de la entidad, como su longitud de contenido o su tipo MIME.</li>
</ul>
---

#### Los encabezados también se pueden agrupar según la forma en que los proxies los manejan:
<ul>
<li style="font-size: 30px;"><b><u>Cabeceras de extremo a extremo</u></b></li>
<p style="font-size: 25px;">Estos encabezados deben transmitirse al destinatario final del mensaje; es decir, el servidor para una solicitud o el cliente para una respuesta. Los proxies intermedios deben retransmitir los encabezados de extremo a extremo sin modificar y los cachés deben almacenarlos.</p>
<li style="font-size: 30px;"><b><u>Cabeceras hop-by-hop</u></b></li>
<p style="font-size: 25px;">Estos encabezados son significativos solo para una conexión de nivel de transporte único y no deben ser retransmitidos por proxies o almacenados en caché. Dichos encabezados son: Conexión, Keep-Alive, Proxy-Authenticate, Proxy-Authorization, TE, Trailer, Transfer-Encoding y Upgrade. Tenga en cuenta que solo los encabezados hop-by-hop se pueden establecer usando el encabezado general Connection.</p>
</ul>
---

### Peticiones HTTP
<p style="font-size: 35px; text-align: left;">Las distintas operaciones que se pueden realizar con HTTP.
Las más comunes son:</p>
- <b><u>GET</u></b>. El método solicita una representación del recurso especificado. Las solicitudes que usan GET solo deben recuperar datos.
- <b><u>POST</u></b>. El método se usa para enviar una entidad al recurso especificado, lo que a menudo causa un cambio en el estado o efectos secundarios en el servidor.
---
### Peticiones HTTP
<p style="font-size: 35px; text-align: left;">Otras, menos comunes:</p>
- <b><u>OPTIONS</u></b>. El método se usa para describir las opciones de comunicación para el recurso objetivo.
- <b><u>DELETE</u></b>. El método elimina el recurso especificado.
- <b><u>TRACE</u></b>. El método realiza una prueba de bucle de mensaje a lo largo de la ruta al recurso de destino.
- <b><u>HEAD</u></b>, <b><u>PUT</u></b>, <b><u>CONNECT</u></b>, <b><u>PATCH</u></b>.
---

### Respuestas HTTP

Los códigos de estado de respuesta HTTP indican si se ha completado satisfactoriamente una solicitud HTTP específica. 
<b>Las respuestas se agrupan en cinco clases:</b>
- <b><u>Respuestas informativas</u></b>
- <b><u>Respuestas satisfactorias</u></b>
- <b><u>Redirecciones</u></b>
- <b><u>Errores de los clientes</u></b>
- <b><u>Errores de los servidores</u></b>
---

### Cookies HTTP

<p style="font-size: 40px; text-align: left;">También llamadas cookies web o cookies de navegador es una pequeña porción de datos que un servidor envía al navegador web del usuario. El navegador guarda estos datos y los envía de regreso junto con la nueva petición al mismo servidor. Las cookies se usan generalmente para decirle al servidor que dos peticiones tiene su origen en el mismo navegador web; lo que permite, por ejemplo, mantener la sesión de un usuario abierta. Las cookies permiten recordar la información de estado en vista a que el protocolo HTTP es un protocolo sin estado.</p>
---
### Cookies HTTP
<p style="font-size: 40px; text-align: left;">Las cookies se utilizan principalmente con <b><u>3 propósitos:</u></b></p>
<ul>
<li style="font-size: 30px;"><b><u>Gestión de sesiones</u></b>. Inicios de sesión, carritos de compras, puntajes de juegos o cualquier otra cosa que el servidor deba recordar</li>
<li style="font-size: 30px;"><b><u>Personalización</u></b>. Preferencias de usuario, temas y otras configuraciones</li>
<li style="font-size: 30px;"><b><u>Seguimiento</u></b>. Grabar y analizar el comportamiento del usuario</li>
</ul>
---
### Cookies HTTP
<p style="font-size: 30px; text-align: left;">
Las cookies se usaron una vez para el almacenamiento general del lado del cliente. Si bien esto era legítimo cuando eran la única forma de almacenar datos en el cliente, hoy en día se recomienda preferir las API de almacenamiento modernas. Las cookies se envían con cada solicitud, por lo que pueden empeorar el rendimiento (especialmente para las conexiones de datos móviles). Las API modernas para el almacenamiento del cliente son la API de almacenamiento web (localStorage y sessionStorage) e IndexedDB.

Al recibir una petición HTTP, un servidor puede enviar una cabecera Set-Cookie junto con la respuesta. Posteriormente el cliente devuelve el valor de la cookie en cada petición al mismo servidor en forma de cabecera de solicitud Cookie. La cookie también puede tener una fecha de expiración determinada, o puede estar restringida a un dominio y path específico.
</p>
---

### Evolución de HTTP
<p style="font-size: 40px; text-align: left;">
HTTP es el protocolo subyacente de la World Wide Web. Inventado por Tim Berners-Lee en los años 1989-1991, HTTP ha visto muchos cambios, manteniendo la mayor parte de la simplicidad y dando mayor forma a su flexibilidad. HTTP ha evolucionado, desde un protocolo inicial para intercambiar archivos en un entorno de laboratorio semiindependiente, hasta el moderno laberinto de Internet, que ahora incluye imágenes, videos en alta resolución y 3D.
</p>
---

### Características de HTTP 2.0
<p style="font-size: 25px; text-align: left;">
HTTP/2 (Protocolo de Transferencia de Hipertexto, versión 2) es un protocolo de red utilizado por la World Wide Web que llegó en 2015 con el objetivo de soportar bien tantas solicitudes al mismo tiempo actualizando HTTP/1.1 (actualización menor en 1999 de la original de 1996, HTTP/1.0), con el que es compatible. Más eficiente, compacto y con menos errores.<br>
El protocolo HTTP / 2 tiene varias diferencias principales de la versión HTTP / 1.1:
</p>

<ul>
<li style="font-size: 25px;"><b><u>Es binario</u></b> en lugar de texto. Ya no se puede leer y crear manualmente a pesar de este obstáculo, ahora se pueden implementar mejores técnicas de optimización.</li>
<li style="font-size: 25px;"><b><u>Es multiplexado</u></b>. Las solicitudes paralelas se pueden gestionar a través de la misma conexión, eliminando el orden y las restricciones de bloqueo del protocolo HTTP / 1.x.</li>
<li style="font-size: 25px;"><b><u>Comprime encabezados</u></b>. Como a menudo son similares entre un conjunto de solicitudes, esto elimina la duplicación y la sobrecarga de los datos transmitidos.</li>
<li style="font-size: 25px;">Permite que un servidor llene datos en un caché del cliente, antes de que se requiera, a través de un mecanismo llamado <b><u>servidor de inserción</u></b>.</li>
</ul>

