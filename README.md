# Práctica 1 – Secuencia de LEDs con Controllino Mega

Este proyecto corresponde a la primera práctica del curso de Control Digital, donde se implementa una secuencia automática de encendido de 9 LEDs utilizando el PLC **Controllino Mega** y el entorno **Arduino IDE**. Se aplica temporización no bloqueante mediante `millis()` y el uso de estructuras para facilitar el control del hardware.

## Objetivo general

Implementar una secuencia continua de encendido de LEDs aplicando lógica estructurada y temporización no bloqueante en un entorno de automatización industrial con el Controllino Mega.

## Descripción

- Se utiliza una estructura `struct Led` para representar cada LED con su pin correspondiente y su estado lógico.
- Los 9 LEDs están definidos en un arreglo tipo `Led`, conectados a las salidas digitales del Controllino.
- El programa enciende un LED a la vez, avanzando en orden secuencial cada 250 ms.
- Una vez que se alcanza el último LED, la secuencia reinicia desde el primero.
- Se evita el uso de la función `delay()` empleando `millis()` para mantener una lógica no bloqueante.

## Vista del hardware

- **PLC utilizado:** Controllino Mega
- **Número de LEDs:** 9
- **Voltaje de operación:** 24 VDC
- **Software:** Arduino IDE con librería `Controllino.h`

## Lógica de temporización

- Variable `intervalo` controla el retardo entre cada cambio de LED.
- La función `millis()` permite comparar el tiempo actual con el último cambio (`tiempoAnterior`), sin bloquear el flujo del programa.
- Esto garantiza un comportamiento continuo, eficiente y sin retardos artificiales.


## Informe

Puedes consultar el desarrollo completo de la práctica, los diagramas, la tabla de asignación de pines y la explicación detallada en:

📄 [`P4_1_conDig.pdf`](./P4_1_conDig.pdf)

## Código

Puedes consultar el codigo detallado en:
📄 [`secuencia.ino`](./secuencia
/secuencia.ino/)

## Autor

E. Bermeo & S. Guillén – Estudiantes de Ingeniería en Telecomunicaciones  
Universidad De Cuenca – Junio 2025
