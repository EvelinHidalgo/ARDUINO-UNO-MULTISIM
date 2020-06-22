**TUTORIAL PARA SIMULAR PROGRAMAS DE ARDUINO UNO EN MULTISIM**

**ARDUINO UNO**

Arduino es una plataforma de creación de electrónica de código abierto, la cual está basada en hardware y software libre, flexible y fácil de utilizar para los creadores y desarrolladores. Esta plataforma permite crear diferentes tipos de microordenadores de una sola placa a los que la comunidad de creadores puede darles diferentes tipos de uso.
Arduino UNO es una placa basada en el microcontrolador ATmega328P. Tiene 14 pines de entrada/salida digital (de los cuales 6 pueden ser usando con PWM), 6 entradas analógicas, un cristal de 16Mhz, conexión USB, conector jack de alimentación, terminales para conexión ICSP y un botón de reseteo. Tiene toda la electrónica necesaria para que el microcontrolador opere, simplemente hay que conectarlo a la energía por el puerto USB o con un transformador AC-DC

**Caracterícas:**

•	Microcontrolador: ATmega328 

•	Voltaje de operación: 5V 

•	Voltaje de entrada (recomendado): 7-12V 

•	Voltaje de entrada (límites): 6-20V 

•	Pines de E/S digitales: 14 (de los cuales 6 proporcionan salida PWM) 

•	Pines de entrada analógica: 6

•	Corriente DC por pin de E/S: 40 mA 

•	Corriente DC para 3.3V Pin: 50 mA

•	Memoria Flash: 32 KB de los cuales 0,5 KB utilizados por el bootloader 

•	SRAM: 2 KB (ATmega328) 

•	EEPROM: 1 KB (ATmega328) 

•	Velocidad de reloj: 16 MHz

**ESPECIFICACIONES ARDUINO UNO**

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img1.jpg)

**1.Botón de reset:** Sirve para inicializar nuevamente el programa cargado en el microcontrolador de la placa. Cuando deje de responder el Arduino Uno es el botón de encendido o apagado para que vuelva a restablecerse. 

**2. Pines o puertos de entrada y salida:** son los pines donde conectar los sensores, componentes y actuadores que necesiten de señales digitales

**3. Pines o puertos de entrada y salida:** son los pines donde conectar los sensores, componentes y actuadores que necesiten de señales digitales.

**4.Puerto USB:** Utilizado tanto para conectar con un ordenador y transferir o cargar los programas al microcontrolador como para dar electricidad al Arduino. También se usa como puerto de transferencia serie a la placa, tanto para transmisión como para recepción de datos.

**5. Chip de interface USB:** es el encargado de controlar la comunicación con el puerto USB.

**6.Reloj oscilador:** es el elemento que hace que el Arduino vaya ejecutando las instrucciones. Es el encargado de marcar el ritmo al cual se debe ejecutar cada instrucción del programa.

**7. Led de encendido:** es un pequeño LED que se ilumina cuando la placa esta correctamente alimentada.

**8. Microcontrolador:** este es el cerebro de cualquier placa Arduino. Es el procesador que se encarga de ejecutar las instrucciones de los programas.

**9. Regulador de tensión:** este sirve para controlar la cantidad de electricidad que se envía a los pines, con lo que asegura que no se estropee lo que conectemos a dichos pines.

**10. Puerto de corriente continua:** este puerto es el que se usa para darle electricidad a la placa si no se usa alimentación USB.

**11. Zócalo de tensión:** aquí estarán los pines con los que alimentaremos nuestro circuito.

**12. Entradas analógicas:** zócalo con distintos pines de entrada analógica que permiten leer entradas analógicas.

**POTENCIA**

La placa puede funcionar con una alimentación externa de 6 a 20 voltios. Sin embargo, si se suministra con menos de 7V, la clavija de 5V puede suministrar menos de cinco voltios y la placa puede ser inestable. Si se utilizan más de 12V, el regulador de voltaje puede sobrecalentarse y dañar la placa. El rango recomendado es de 7 a 12 voltios.

**Pines de potencia**

•	VIN:El voltaje de entrada a la placa Arduino cuando está usando una fuente de alimentación externa (a diferencia de los 5 voltios de la conexión USB u otra fuente de alimentación regulada). Puede suministrar tensión a través de esta clavija o, si lo hace a través de la toma de corriente, acceder a ella a través de esta clavija. 

•	5V: Esta clavija emite un 5V regulado desde el regulador de la tarjeta. La tarjeta puede alimentarse ya sea desde el conector de alimentación de CC (7 – 12 V), el conector USB (5 V) o la clavija VIN de la tarjeta (7-12 V). La alimentación de tensión a través de las clavijas de 5V o 3,3V puentea el regulador y puede dañar la placa.  

•	3V3: Una alimentación de 3,3 voltios generada por el regulador de a bordo. El consumo máximo de corriente es de 50 mA.

•	GND: Pins de tierra.

**ENTRADA Y SALIDA, INPUT AND OUTPUT**

Cada uno de los 14 pines digitales de la Uno puede utilizarse como entrada o salida, utilizando las funciones pinMode(), digitalWrite() y digitalRead(). Funcionan a 5 voltios. Cada clavija puede proporcionar o recibir un máximo de 40 mA y tiene una resistencia pull-up interna (desconectada por defecto) de 20-50 kOhms. Además, algunos pines tienen funciones especializadas: 

•	Serial: 0 (RX) y 1 (TX). Se utiliza para recibir (RX) y transmitir (TX) datos en serie TTL. Estos pines están conectados a los pines correspondientes del chip Serial ATmega8U2 USB-to-TTL.

•	Interrupciones externas: 2 y 3. Estos pines pueden configurarse para activar una interrupción en un valor bajo, un flanco ascendente o descendente, o un cambio de valor. Vea la función attachInterrupt () para más detalles. 

•	PWM: 3, 5, 6, 9, 10 y 11. Proporciona salida PWM de 8 bits con la función analogWrite (). 

•	SPI: 10 (SS), 11 (MOSI), 12 (MISO), 13 (SCK). Estos pines soportan la comunicación SPI utilizando la biblioteca SPI.

•	LED 13: Hay un LED incorporado conectado al pin 13 digital. Cuando la clavija es de valor ALTO, el LED se enciende, cuando la clavija es BAJA, se apaga. 
La Uno tiene 6 entradas analógicas, etiquetadas de A0 a A5, cada una de las cuales proporciona 10 bits de resolución (es decir, 1024 valores diferentes). Por defecto miden de tierra a 5 voltios, aunque es posible cambiar el extremo superior de su rango usando el pin AREF y la función analogReference(). 

**PINES TIENEN FUNCIONALIDAD ESPECIALIZADA**

•	TWI: Pin A4 o SDA y pin A5 o SCL. Soporta la comunicación TWI usando la biblioteca Wire.

•	AREF: Tensión de referencia para las entradas analógicas. Se utiliza con analogReference (). 

•	RESET: Lleve esta línea a un nivel BAJO para reiniciar el microcontrolador. Típicamente se usa para añadir un botón de reinicio a los escudos que bloquean el que está en la placa.

**DIAGRAMA PINOUT ARDUINO UNO**

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img2.jpg)

**ARDUINO UNO PINOUT – FUENTE DE ALIMENTACIÓN **

Hay 3 formas de alimentar el Arduino Uno: 

•	Barrel Jack: El Barrel Jack, o DC Power Jack puede ser usado para alimentar tu placa Arduino. El conector cilíndrico suele estar conectado a un adaptador de pared. La tarjeta puede ser alimentada por 5-20 voltios, pero el fabricante recomienda mantenerla entre 7-12 voltios. Por encima de 12 voltios, los reguladores podrían sobrecalentarse, y por debajo de 7 voltios, podrían no ser suficientes.

•	VIN Pin: Este pin se utiliza para alimentar la placa Arduino Uno utilizando una fuente de alimentación externa. El voltaje debe estar dentro del rango mencionado anteriormente. 

•	Cable USB :cuando se conecta a la computadora, proporciona 5 voltios a 500mA.

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img3.jpg)

Hay un diodo de protección de polaridad que se conecta entre el positivo de la clavija del barril y la clavija VIN, con una capacidad nominal de 1 amperio.

Cuando se alimenta un circuito a través de la toma de barril o VIN, la capacidad máxima disponible está determinada por los reguladores de 5 y 3.3 voltios a bordo del Arduino. 

•	5v y 3v3 Proporcionan 5 y 3.3v regulados para alimentar componentes externos de acuerdo con las especificaciones del fabricante.

•	GND En el pinout de Arduino Uno, puedes encontrar 5 pines GND, todos ellos interconectados. 
Las clavijas GND se utilizan para cerrar el circuito eléctrico y proporcionar un nivel de referencia lógico común en todo el circuito. Asegúrate siempre de que todos los GNDs (del Arduino, periféricos y componentes) estén conectados entre sí y tengan una conexión a tierra común. 

•	RESET – reinicia el Arduino

•	IOREF – Este pin es la referencia de entrada/salida. Proporciona la referencia de tensión con la que funciona el microcontrolador.

**ARDUINO UNO PINOUT – ANALOG IN**

 La placa Arduino Uno tiene 6 pines analógicos, que utilizan ADC (Convertidor de Analógico a Digital). Estos pines sirven como entradas analógicas, pero también pueden funcionar como entradas o salidas digitales
 
![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img4.jpg)

**Conversión de analógico a digital**

 ADC son las siglas de Analog to Digital Converter. El ADC es un circuito electrónico utilizado para convertir señales analógicas en señales digitales. Esta representación digital de señales analógicas permite al procesador, que es un dispositivo digital, medir la señal analógica y utilizarla durante su funcionamiento. 
Los pines Arduino A0-A5 son capaces de leer tensiones analógicas. En Arduino el ADC tiene una resolución de 10 bits, lo que significa que puede representar una tensión analógica de 1.024 niveles digitales. El ADC convierte el voltaje en bits que el microprocesador puede entender.

**ARDUINO UNO PINOUT – DIGITAL PINS**

•	Los pines 0-13 del Arduino Uno sirven como pines de entrada/salida digital.

•	El pin 13 del Arduino Uno está conectado al LED incorporado. 

•	En el Arduino Uno – los pines 3,5,6,9,10,11 tienen capacidad PWM.
 Es importante tener en cuenta: 
 
•	Cada clavija puede proporcionar hasta 40 mA máx. Pero la corriente recomendada es de 20 mA. 

•	La corriente máxima absoluta proporcionada de todos los pines juntos es de 200 mA.

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img5.jpg)

**MULTISIM 14.0**

Multisim™ es un software estándar en industria para diseño de circuitos y simulación SPICE para electrónica de potencia, analógica y digital en la educación y la investigación.

El software Multisim™ integra simulación SPICE estándar en la industria con un entorno esquemático interactivo para visualizar y analizar al instante el comportamiento de los circuitos electrónicos. Su interfaz intuitiva ayuda a los profesores a reforzar la teoría de circuitos y a mejorar la retención de la teoría en todo el plan de estudios de ingeniería. Al añadir simulación potente de circuitos y análisis al flujo de diseño, Multisim™ ayuda a los investigadores y diseñadores a reducir las iteraciones de prototipos de tarjeta de circuito impreso (PCB) y a ahorrar los costos del desarrollo.

**MANUAL DE USUARIO**

1.Ingresar a la página oficial de Nacional Instruments en el siguiente link https://www.ni.com/es-cr/support/documentation/supplemental/14/multisim-templates-for-custom-arduino-shields.html

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img6.jpg)

2.Al ingresar a la página buscar la sección de DESCARGAS y proceder a descargar el archivo .zip

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img7.jpg)

3. Crear una nueva carpeta  que en este caso se llamará “Arduino Library” en la carpeta que se genera  al instalar el software Multisim donde se guardan los diseños de circuitos.

En este caso:

3.1Disco (C)

3.2Archivos de programa (x86)

3.3National Instruments

3.4Circuit Design Suite 14.0

3.5Arduino Library


![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img8.jpg)

4.Copiar y pegar el archivo .zip en la carpeta Arduino Library


![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img9.jpg)

5.Extraer el archivo .zip y se generaran  varias carpetas que contienen plantillas de tipos de Arduinos

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img10.jpg)

6.Abrir Multisim 14.0

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img11.jpg)

7. En la parte superior izquierda dar click en FILE y OPEN.

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img12.jpg)

8.Buscar la carpeta creada con anterioridad “Arduino Library”, click en abrir y se desplegará una serie de carpetas a escoger.

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img13.jpg)

9.Las carpetas desplegadas contiene diferentes tipos de arduinos en este caso se escogió el ARDUINO UNO, click en abrir.

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img14.jpg)

10. Finalmente se a generado un ARDUINO UNO en Multisim.

![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img15.jpg)
![](https://github.com/EvelinHidalgo/ARDUINO-UNO/blob/master/img/img16.jpg)

**BIBLIOGRAFÍA**

[1] Descubre Arduino.com.(2014). ARDUINO UNO, PARTES, COMPONENTES, PARA QUÉ SIRVE Y DONDE COMPRAR.Recuperado de:https://descubrearduino.com/arduino-uno/

[2] National Instruments.(2020).¿Qué es Multisim™?.Recuperado de: https://www.ni.com/es-cr/shop/electronic-test-instrumentation/application-software-for-electronic-test-and-instrumentation-category/what-is-multisim.html#:~:text=Multisim%E2%84%A2%20es%20un%20software,la%20educaci%C3%B3n%20y%20la%20investigaci%C3%B3n.
