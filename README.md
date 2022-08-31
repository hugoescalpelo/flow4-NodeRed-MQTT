# flow4-NodeRed-MQTT
Este repositorio contiene el flow 4 del curso de NodeRed, visto en en los contenidos de Internet de las cosas de Codigo IoT en edu.codigoiot.com

## Introducción

Este flow consiste en un tablero que presente la información de temperatura y humedad locales. Este flow recibe la información por MQTT con un broker local.

## Material Necesario

Para realizar este flow necesitas lo siguiente

- [Ubuntu 20.04](https://releases.ubuntu.com/20.04/)
- [NodeJS](https://nodejs.org/es/)
    - [NPM](https://www.npmjs.com/)
    - [NodeRed](https://nodered.org/docs/getting-started/local)
    - [Nodos Dashboard](https://flows.nodered.org/node/node-red-dashboard)
- [Mosquitto](https://mosquitto.org/)

## Material de referencia

En los siguientes enlaces puedes encontrar cursos en la plataforma de edu.codigoiot.com que te permitirán realiar las configuraciones necesarias

- [Instalación de Virutal Box y Ubuntu 20.04](https://edu.codigoiot.com/course/view.php?id=812)
- [Instalación de NodeRed](https://edu.codigoiot.com/course/view.php?id=817)
- [Introducción a NodeRed](https://edu.codigoiot.com/course/view.php?id=278)
- [Introducción a Mosquitto](https://edu.codigoiot.com/course/view.php?id=851)

## Instrucciones

### Requisitos previos

Para que este flow funcione, debes cumplir con los siguientes requisitos previos
1. Instalación de NodeJS. Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM
2. Instalación de NodeRed. La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2
3. Instalar los nodos node-red-dashboard. Para ello, dirigete a la opcion "Manage Palet" de NodeRed y en la pestaña Install busca node-red-dashboard. Finalmente haz clic en instalar.
4. Instalación de Broker local Mosquitto MQTT.

### Instrucciones de preparación del entorno

Para ejecutar este flow, es necesario lo siguiente
1. Arrancar NodeRed con el comando `node-red`
2. Importar el flow del repositorio
3. Hacer clic en el boton Deploy

### Instrucciones de operación

- Para observar el resutlado de este flow, abre un navegador y dirígete a localhost:1880/ui
-  Enviar por MQTT un mensaje que contenga un JSON con las variables ID, temp y hum

### Notas

- Este Flow se suscribe al tema codigoIoT/Mor/mqtt/flow4
- El mensaje mqtt usado para probar este flow es `mosquitto_pub -h localhost -t codigoIoT/Mor/mqtt/flow4 -m '{"ID":"Hugo Vargas","temp":18,"hum":78}'`
- Para que la gráfica historica muestre información, deben enviarse al menos 2 puntos

## Resultados

A continuación puedes ver los nodos del flow.
![](https://github.com/hugoescalpelo/flow4-NodeRed-MQTT/blob/main/Nodos.png?raw=true)

A continuación puede ver el tablero resultante.

![](https://github.com/hugoescalpelo/flow4-NodeRed-MQTT/blob/main/Dashboard.png?raw=true)

## Evidencias

- [YouTube](https://youtu.be/84X-jtUX414)

# Créditos

Desarrollado por Hugo Escalpelo
- [hugoescalpelo.com](https://hugoescalpelo.com/)
- [Página en Facebook](https://www.facebook.com/Hugo-Escalpelo-Profesional-337708683840136)
- [GitHub](https://github.com/hugoescalpelo)