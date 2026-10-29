CAMBIOS PARA CONTROLAR EL QUINTO LED POR UART

Archivos modificados:
- Core/Src/main.c
- Core/Inc/main.h

Comandos UART (USART1 a 9600 baudios, 8N1):
- LED ON  -> enciende el quinto LED conectado a PA3
- LED OFF -> apaga el quinto LED conectado a PA3

En Proteus:
1. Agrega un LED y una resistencia de 220 a 330 ohmios.
2. Conecta PA3 -> resistencia -> ánodo del LED.
3. Conecta el cátodo del LED a GND.
4. Comprueba que la referencia del microcontrolador del esquema coincida con el firmware STM32F401 configurado en el proyecto.
5. En el terminal UART usa 9600 baudios, 8 bits, sin paridad y 1 bit de parada.
6. Envía LED ON o LED OFF. Se aceptan mayúsculas o minúsculas; se recomienda enviar el comando seguido de Enter.

NOTA:
El código de firmware fue actualizado para inicializar PA3 como salida, procesar los comandos recibidos y responder por UART.
El esquema Proteus original se conserva; el quinto LED debe agregarse manualmente siguiendo las conexiones indicadas.
