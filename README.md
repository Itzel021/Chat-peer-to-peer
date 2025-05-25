# 📌Chat-Peer-to-Peer-Multicast

## Índice
- [Definición](#definición)
- [Características](#características)
- [Requisitos](#requisitos)
- [Ejecución](#ejecución)
- [Autores](#autores)

## 💻 Definición
<p align="justify">
Una red P2P (Peer-to-Peer) representa un ecosistema de comunicación donde todos los nodos o usuarios de la red operan en igualdad de condiciones, siendo capaces de asumir tanto funciones de servidor como de cliente de manera simultánea. La arquitectura peer-to-peer (P2P) ha emergido como un paradigma poderoso y descentralizado para compartir recursos entre múltiples nodos de una red. En este contexto, el desarrollo de un sistema en Java que facilite la comunicación y el intercambio de archivos entre pares resulta fundamental para comprender los principios de esta arquitectura y la implementación de algoritmos de coordinación como el algoritmo Bully (Abusón). 
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/4e71d3b1-64b0-4521-91dc-ca5b362c7f8f" alt="1200х600-Peer-to-Peer-Network" width="600">
</p>

## ✨ Características
<p align="justify">
<ul>
<li>Descentralización: No existe un servidor central que coordine las interacciones entre los usuarios. En cambio, todos los nodos de la red operan como servidores y clientes a la vez, posibilitando que la información y los servicios circulen y sean compartidos de forma descentralizada.</li>

<li>Participación activa: Los usuarios deben involucrarse activamente en la red para contribuir con recursos y recibirlos a su vez. En otras palabras, un usuario no solo consume recursos, sino que también actúa como proveedor de estos para otros participantes.</li>

<li>Gestión de la conexión: La gestión de conexiones y la transferencia de archivos se llevan a cabo mediante acuerdos entre los usuarios, sin requerir la intervención de un servidor central que dicte estas interacciones.</li>

<li>Compartición de recursos: Los usuarios tienen la capacidad de compartir una variedad de recursos, desde archivos hasta servicios y conocimientos, con otros miembros de la red.</li>

<li>Algoritmo de elección (Bully): Utilizado en sistemas distribuidos para seleccionar un coordinador o líder dinámicamente a partir de un grupo de procesos informáticos distribuidos.</li>
</ul>
</p>

🧠 ¿Qué es y cómo funciona el algoritmo de Bully?
<p align="justify">
El algoritmo de <strong>Bully</strong> (en español, "abusón") es un protocolo de elección de coordinador usado en sistemas distribuidos, donde es fundamental identificar un nodo líder que se encargue de tareas de coordinación, como la gestión de recursos compartidos o la sincronización de procesos. Este algoritmo es particularmente útil en redes P2P donde no hay un servidor central.

Cuando un proceso detecta que el coordinador actual ha fallado (por ejemplo, al no recibir respuestas en cierto tiempo), inicia una elección enviando un mensaje a todos los procesos con un identificador mayor al suyo. Si ninguno de estos responde, el proceso que inició la elección se declara a sí mismo como el nuevo coordinador. Sin embargo, si alguno responde, ese otro proceso toma el control de la elección y repite el procedimiento, eliminando así a los procesos con identificadores menores (de ahí el nombre "Bully").

Este procedimiento garantiza que el proceso con el identificador más alto termine siendo el coordinador, ya que es capaz de "intimidar" a los demás al responder y tomar el control del proceso de elección.
</p>

<p align="justify">
<strong>Funcionamiento general:</strong>
<ul>
  <li>Un proceso detecta que el coordinador ha fallado.</li>
  <li>Envía un mensaje de elección a todos los procesos con ID mayor.</li>
  <li>Si nadie responde, se proclama coordinador y envía un mensaje a todos anunciándolo.</li>
  <li>Si alguno responde, este toma el control y repite el proceso.</li>
  <li>El proceso con el ID más alto será finalmente el coordinador.</li>
</ul>
</p>

## 📢 Requisitos
- NetBeans IDE 17 o 19
- JDK 19

## 🚀 Ejecución
<p align="justify">
<ul>
<li>Para el archivo .JAR:
  <ul>
    <li>Descargar el archivo.</li>
    <li>Ejecutar el archivo .jar</li>
    <li>Cada ejecución del archivo .jar crea una nueva instancia (peer).</li>
    <li>Ingresa el nombre del nuevo par.</li>
    <li>Envia mensajes o archivos a la red.</li>
    <li>Descarga archivos y visualiza los pares conectados.</li>
  </ul>
</li>
</ul>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/0d008839-a350-4f77-8397-da97198c29b3" alt="Captura de pantalla 2024-08-12 214757" width="600">
</p>

## 👥🤯 Autores
<p align="justify">
<ul>
<li>Itzel Daniela Martínez Carrera</li>
<li>Evelyn Dolores Flores Lechuga</li>
</ul>
</p>
