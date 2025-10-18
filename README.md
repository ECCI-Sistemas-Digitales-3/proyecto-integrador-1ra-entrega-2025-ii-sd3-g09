[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=21147995&assignment_repo_type=AssignmentRepo)
# Proyecto integrador 1ra Entrega

## Integrantes

Maria Paula Fierro Barrios

Astrid Catalina Ortiz Lopez

Camilo Suarez Camacho

## Arquitectura propuesta

Propuesta de implementación en Node-RED
La propuesta consiste en incluir dos sensores de temperatura que permitan visualizar lecturas independientes en el panel de control (Dashboard).
Además, se agrega un indicador visual asociado al primer sensor, con el propósito de controlar una resistencia de calentamiento de la siguiente manera:

- Cuando el sensor 1 detecta una temperatura por debajo del umbral establecido, la resistencia se activa (encendida).
- Cuando la temperatura medida alcanza o supera el límite configurado, el indicador se enciende y simultáneamente la resistencia se apaga, evitando un sobrecalentamiento del sistema.


Esta lógica permite automatizar el control térmico mediante el uso de condiciones (switch o function nodes) en Node-RED, combinando la lectura de los sensores con salidas digitales o visuales.


<p align="center">
  <img src="image.png" alt="Diagrama Node-RED" width="70%">
  <br>
  <strong>Figura 1. Diagrama Node-RED</strong>
</p>


<p align="center">
  <img src="image-1.png" alt="Diagrama Node-RED 1" width="45%">
  <img src="image-2.png" alt="Diagrama Node-RED 2" width="40%">
  <br>
  <strong>Figuras 2. Sensores</strong>
</p>

## Periférico a trabajar

Conexión de los sensores a la ESP32

Dentro de las pruebas realizadas, se conectó la placa ESP32 a dos sensores de temperatura, utilizando los pines 33 y 25 como entradas de lectura.
La configuración se realizó siguiendo el esquema mostrado en las Figuras 3 y 4, donde se observa el cableado correspondiente y la distribución de los componentes sobre la protoboard.

Estas conexiones permitieron obtener mediciones simultáneas de temperatura desde ambos sensores, las cuales fueron posteriormente visualizadas en la interfaz desarrollada en Node-RED.

<p align="center">
  <img src="image-3.png" alt="Conexión del sensor 1 a la ESP32" width="50%">
  <br>
  <strong>Figura 3. Conexión a la ESP32 </strong>
</p>

<p align="center">
  <img src="image-4.png" alt="Conexión del sensor 2 a la ESP32" width="50%">
  <br>
  <strong>Figura 4. Diagrama esquemático</strong>
</p>


## Avances

Pruebas funcionales

Dentro de los avances realizados, se efectuaron pruebas simultáneas con los dos sensores de temperatura (PT100) conectados a la ESP32.
Estas pruebas se ejecutaron utilizando el entorno Thonny, donde se cargó y corrió el código correspondiente para la lectura de ambos sensores.

En la consola de Thonny fue posible observar en tiempo real los valores de temperatura detectados por las dos PT100.
Posteriormente, estos datos se visualizaron en la interfaz de Node-RED, evidenciando que ambos sensores enviaban valores de temperatura similares, lo cual confirma el correcto funcionamiento de la comunicación.

<p align="center">
  <img src="image-5.png" alt="Visualización de lecturas PT100 en Thonny y Node-RED" width="60%">
  <br>
  <strong>Figura 5. Visualización de las lecturas de las PT100 en Thonny</strong>
</p>
