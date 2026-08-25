# ESPWROOM32-PRIMERA-ACTIVIDAD # 
Definición, Estructura y Arquitectura
El ESP-WROOM-32 es un módulo genérico de desarrollo altamente integrado que provee conectividad Wi-Fi y Bluetooth Clásico y de Baja Energía - BLE. Está diseñado tanto para aplicaciones de baja potencia como redes de sensores, como para tareas exigentes como transmisión de audio o procesamiento de datos.

Estructura: El módulo encapsula físicamente el chip SoC ESP32, un oscilador de cristal de 40 MHz, una antena en el PCB o conector para antena externa y memoria Flash externa usualmente de 4 MB para almacenar programas.

Arquitectura: Su núcleo es el potente microprocesador Tensilica Xtensa Dual-Core de 32 bits LX6. Opera con una frecuencia de reloj ajustable entre 80 MHz y 240 MHz, e incluye un coprocesador de ultra bajo consumo (ULP) ideal para monitorear sensores básicos mientras el sistema principal está en modo de suspensión profunda.

Características, Conexiones y Pines
La placa resalta por su extensa variedad de interfaces de hardware, lo que la hace sumamente versátil para conectar múltiples módulos externos:

Conectividad: Integra Wi-Fi (802.11 b/g/n) y Bluetooth v4.2 BR/EDR y BLE.

Pines (GPIO): Dispone de hasta 34 pines de propósito general. Estos pines son multiplexados, lo que significa que un mismo pin puede cumplir diferentes funciones (UART, SPI, I2C, etc.) según se programe.

ADC (Convertidor Analógico a Digital): Posee hasta 18 canales ADC con una resolución de 12 bits, lo que permite leer voltajes de sensores analógicos de forma precisa.

PWM (Modulación por Ancho de Pulsos): Cuenta con controladores PWM por hardware que se pueden asignar a casi cualquier pin, ideales para controlar el brillo de LEDs o la velocidad de servomotores.

DAC (Convertidor Digital a Analógico): Incluye 2 canales DAC de 8 bits para convertir señales digitales internas en voltajes analógicos reales.

Programación en C/C++ (Arduino IDE o ESP-IDF)

Al programar el ESP32 en C o C++, la principal ventaja radica en su rendimiento superior. Al ser lenguajes compilados y de bajo nivel, permiten una ejecución extremadamente rápida y un aprovechamiento máximo de los recursos, brindándo un control total sobre el hardware y la memoria del microcontrolador. Además, cuentan con un ecosistema gigantesco, por lo que se puede encontrar librerías y documentación para conectar casi cualquier sensor o módulo del mercado.

Sin embargo, este enfoque también presenta sus desventajas. La curva de aprendizaje suele ser más pronunciada debido a una sintaxis más estricta y a que el código tiende a ser más complejo. A esto se suma que el proceso de desarrollo puede sentirse más lento, ya que cada vez que se realiza un cambio en el código o se quiere hacer una prueba, es necesario compilar y cargar todo el programa nuevamente en la placa.

Programación en MicroPython

Al utilizar MicroPython destaca por ofrecer una sintaxis limpia, intuitiva y muy fácil de leer, lo que lo hace excelente para novatos. Su mayor ventaja es que acelera enormemente el tiempo de desarrollo y el prototipado rápido. Al incluir una consola interactiva (REPL), puedes ejecutar líneas de código y probar componentes al instante, sin necesidad de compilar nada.

En cuanto a sus desventajas, la principal limitación de MicroPython es la velocidad. Al ser un lenguaje interpretado, la ejecución del código es notablemente más lenta en comparación con C/C++. Además, la máquina virtual de Python requiere una porción significativa de la memoria base del ESP32 para funcionar, y al abstraer tanto el código, se pierde la capacidad de tener un control minucioso de bajo nivel para exprimir al máximo las capacidades del hardware.
