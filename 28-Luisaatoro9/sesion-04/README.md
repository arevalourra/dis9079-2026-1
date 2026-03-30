# sesion-04

lunes 30 marzo 2026

**Claude Shannon invented the future** 

* **https://people.math.harvard.edu/~ctm/home/text/others/shannon/entropy/entropy.pdf**
<img width="800" height="588" alt="Captura de pantalla 2026-03-30 162936" src="https://github.com/user-attachments/assets/448bc899-d79b-4fbe-8bc5-6c49af8c950a" />
<img width="800" height="565" alt="image" src="https://github.com/user-attachments/assets/fd8d85e5-f090-4a0e-a099-e24f6ce67f9e" />

# **Codigo RecibirArduino**
https://github.com/user-attachments/assets/e2b217d5-daf4-4f3e-91c7-cc4d67c35b1f

# **UNO R4 WiFi Network Examples**
https://docs.arduino.cc/tutorials/uno-r4-wifi/wifi-examples/#wi-fi-udp-send-receive-string
1. Conectarte a internet: Cómo hacer que tu placa use el Wi-Fi de tu casa o de la UDP.
2. Web Server: Cómo crear una página web interna que puedas ver desde tu celular para prender luces, por ejemplo.
3. Network Scan: Cómo hacer que el Arduino busque redes Wi-Fi cerca.


1. Lo que estás usando (MQTT/TCP): Es como una llamada por teléfono. Te aseguras de que la otra persona te escucha y si algo se corta, lo repites hasta que llegue bien. Es seguro pero un poco más lento.
2. UDP: Es como tirar volantes desde un avión. ✈️ Mandas la información súper rápido, pero no te importa si alguien no los agarra o si algunos se pierden en el camino.

## Apuntes de la Sesión: Protocolos y Conectividad
Durante esta sesión trabajamos en la conexión inalámbrica de la placa **Arduino UNO R4 WiFi** utilizando el protocolo MQTT. 

### 1. Conceptos Clave 

1. MQTT (Message Queuing Telemetry Transport) > Es el protocolo que estamos usando en el taller. Funciona bajo un modelo de publicación/suscripción. Es ideal para IoT porque es ligero y eficiente para enviar datos entre sensores y actuadores. > 
UDP (User Datagram Protocol)> Es un protocolo de comunicación rápido pero "no confiable" (no asegura que todos los datos lleguen). Se diferencia del que usamos nosotros en que no establece una conexión fija antes de enviar datos. Dato: No confundir con las siglas de nuestra universidad.

2. Diferencia entre ID y Username en MQTT mqttId:Es el identificador único de mi placa en la red. Si dos placas tienen el mismo ID, hay conflicto. * Username: Es la credencial de seguridad (en nuestro caso `dis9079`) que nos permite acceder al servidor (broker). 

3. Código de Recepción y Envío Logré cargar el código `recibirArduino.ino` con éxito. La placa se conecta al broker `192.168.0.100` y envía un mensaje alternando un "numerito" entre 0 y 1 cada 5 segundos.

💡WiFi Chat Server

Convierte tu Arduino en un pequeño "servidor de mensajes". Imagina que es como crear tu propia sala de chat de WhatsApp, pero que solo funciona dentro de la red Wi-Fi donde está conectada la placa.

    ¿Cómo funciona? Alguien se conecta a la dirección IP de tu Arduino (usando algo llamado Telnet) y puede escribir mensajes que aparecen en tu Monitor Serial.
    ¿Qué hace el código? Recibe lo que un usuario escribe y se lo "rebota" (echo) para que los demás también lo vean.

Diferencia con lo hice:

    El código anterior (MQTT): Usa un intermediario (el "broker") para enviar y recibir datos. Es el estándar para conectar miles de dispositivos de forma ordenada.
    Este código (Chat Server): Es una conexión directa. Tú eres el dueño del servidor. Es un ejemplo clásico para aprender cómo funciona la arquitectura de internet (Cliente-Servidor).

Explicando la solemne 1
