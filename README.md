# TRABAJO PRÁCTICO FINAL

## MONITOR DE SIGNOS VITALES

**Se debe implementar un monitor de signos vitales que muestre el estado de los parámetros vitales en un celular y alertar al paciente mediante mensajes de voz pregrabados en caso de encontrarse próximo a una situación de riesgo.**

**Funcionamiento**

El monitor consiste de 3 sensores que monitorean 3 variables vitales

1. ECG-AFE (electrocardiogram (ECG) analog front end (AFE))
2. Oxímetro de pulso (SpO 2 )
3. Sensor de temperature corporal

El monitor deberá graficar en forma permanente la información proveniente de la señal generada por el ECG-AFE y la señal generada por el Oxímetro de pulso.
Además, se deberá mostrar numéricamente los latidos por minuto (BPM), saturación de oxígeno en sangre (SpO 2 ) y la temperatura corporal.

Se deberán generar alertas mediante mensajes de voz pregrabados cuando las variables están fuera de rango. Los mensajes pregrabados deberán estar en formato MP3.

El monitor deberá enviar (via bluetooth) los valores de las variables antes mencionadas a un celular o Tablet, si está disponible.

## Requisitos obligatorios

### Para que el trabajo esté aprobado debe cumplir con los siguientes requisitos:

**Almacenamiento de los mensajes**
Los mensajes de voz pregrabados deberán residir en la flash, en formato MP3.

**Reproducción de audio**
La reproducción del audio se realizará mediante un DAC I2S conectado a la placa FRDNK64F cuya salida deberá poder conectarse a un auricular o parlante.

**Visualización**
El equipo debe visualizar la información generada por los sensores en forma gráfica como numérica en un celular o Tablet.

**Sensores**
ECG: Electrocardiógrafo para la obtención de la señal cardiaca (Ej: AD8232)
SPO2: Oxímetro de pulso (Ej.:MAX30105)
Sensor de temperatura corporal (Ej.:MAX30205)

**Interface Bluetooth**
La interface bluetooth se hará con un módulo HC05 o similar.

**Placa propia**
El microcontrolador con su electrónica asociada deben estar montados en una placa de diseño propio. No está permitido utilizar la placa FRDM-K64F.

## Funcionalidad opcional

**Display**

Display LCD TFT Táctil de 240x320 pixeles con interface SPI.

**Conectividad IoT**

Mediante un Modulo ESP8266 (WiFi) se podrán publicar los valores de los parámetros usando ThingSpeak y/o Nodered.

**Modo bajo consumo**

El equipo debe poder encenderse y apagarse. En modo apagado el consumo medio de corriente debe ser menor a 50 A (alimentado desde una fuente de 5V).

### Reglas

**Fecha de vencimiento**

Este trabajo se puede entregar hasta diciembre del 2020 (inclusive). Si para la fecha mencionada él trabajo no fue aprobado, el alumno deberá resolver un enunciado nuevo.

**Propiedad Intelectual**

Se permite utilizar código y librerías de terceras partes, así como el _SDK_ y _Processor Expert_ del FRDM-K64F. Es obligatoria la entrega de un documento dónde se enumere todo el material externo utilizado (que no sea generación propia).

### Entrega y Evaluación

La entrega será una exposición oral de 30 minutos donde se presente:

- Funcionamiento del equipo: mostrar todas las prestaciones, correcta reproducción y visualización de la música y consumo al estar apagado.
- Diseño de firmware: estructura, drivers utilizados, medición del uso de CPU y cumplimiento de requerimientos temporales.
- Diseño de hardware: esquemático y conexionado del MCU en la placa.

La calidad y claridad de la presentación también será evaluada.

## ANEXO

### Librerías

#### MP3:

- Introducción: https://www.helixcommunity.org/projects/datatype/mp3dec

- Librería con código fuente y también pre-compilada para Cortex-M4: adjunto

- Para usarla, sólo se necesitan los headers de la carpeta "pub" y linkear
    "libhelix.a".
