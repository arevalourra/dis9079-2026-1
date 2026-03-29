# sesion-03

lunes 23 marzo 2026


## Comunicación entre dispositivos
El objetivo principal del proyecto es lograr comunicación entre dos dispositivos distintos, específicamente microcontroladores.

- Arduino Uno R4 WiFi → envía datos  
- Raspberry Pi Pico 2 W → recibe datos  

La meta no es solo enviar información, sino que el sistema completo funcione correctamente (emisor + receptor).

## Microcontroladores y plataformas

### Raspberry Pi Pico 2 W
Placa de desarrollo orientada a proyectos electrónicos e IoT.

**Características:**
- Chip: RP2350  
- Doble núcleo  
- Wi-Fi (802.11n)  
- Bluetooth 5.2  
- Bajo costo y alto rendimiento  

La fundación Raspberry Pi nace en 2009 con el objetivo de crear computadores accesibles.

### Arduino vs Raspberry Pi

| Arduino | Raspberry Pi |
|--------|-------------|
| Microcontrolador | Sistema más complejo |
| Simple | Más potente |
| Tareas específicas | Procesos más avanzados |

### Otras plataformas
- BeagleBoard → hardware open source  
- Bela → audio en tiempo real  
- Electro-Smith (Daisy) → audio avanzado  
- Monome / Critter & Guitari → instrumentos digitales  
- NIME → investigación en interfaces musicales  

## Historia breve de la computación

- Harvard Mark I → computador electromecánico  
- Mainframe → computadores centrales  
- Atari 2600 → videojuegos  
- Commodore 64 → computador personal  
- ZX Spectrum → computador doméstico  

## Entorno de desarrollo

### Visual Studio Code
Se usará como entorno principal.

**Lenguajes:**
- C++
- Python
- MicroPython

**Conceptos clave:**
- Extensiones → agregan funciones  
- SDK → herramientas de desarrollo  
- Build → compilación del código  

## Estructura de proyecto

- `.vscode` → configuración  
- `build` → archivos compilados  
- `.gitignore` → archivos no compartidos  
- `main.cpp` → archivo principal  
- `CMakeLists.txt` → configuración de compilación  

Todo comienza en `main()` y se ejecuta en orden.

## Lógica de programación

### Arduino
```cpp
void setup() {
}

void loop() {
}
```

### Raspberry Pi Pico

```cpp
int main() {
    while (true) {
        // bucle infinito
    }
}
```
## Protocolos de comunicación
SPI
- Comunicación rápida
- Usa varios pines
- Ideal para pantallas


I2C
- Menos cables
- Más simple
- Permite múltiples dispositivos

## Solemne 1

Fecha: 6 de abril

### Puntaje
- Base: 1 punto
- Total: 6 puntos
### Individual
- Presentación oral
- Bitácora (texto + visual)
- Aporte al README
### Grupal
- Diagrama de flujo
- Código (envío y recepción)
- Funcionamiento
### Evaluación funcional
- 1.0 → envía y recibe
- 0.5 → solo una función
- 0.3 → intentos
- 0.0 → no funcional
