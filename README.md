# Arduino Serial Logger Example

## Descripción
Este proyecto implementa una comunicación en Simulink para adquirir datos del sensor BNO055 conectado a un Arduino DUE. La frecuencia de muestreo es de 100 Hz, y los datos adquiridos se envían a través del puerto serie en un formato de trama estructurado. La intención es que esta información pueda ser almacenada en un datalogger para su posterior análisis.

## Componentes Utilizados
- **Arduino DUE**
- **Sensor BNO055** (Acelerómetro, Giroscopio y Magnetómetro)
- **Simulink** (MATLAB)

## Configuración del Proyecto
Para garantizar el correcto funcionamiento del proyecto, es necesario configurar los siguientes parámetros en Simulink:

### Configuración del Puerto Serie
- **Baud Rate:** 115200 bps
- **Formato de salida:** ASCII

### Configuración en Simulink
- **Frecuencia de muestreo:** 100 Hz
- **Formato de trama:** `"A,%.3f,%.2f,%.2f,%.2f,%.2f,%.2f,%.2f,%.2f,%.2f,Z\n"`

### Simulink: Configuración en Code Generation
- **Language Standard:** C99

## Estructura del Proyecto en Simulink
1. **Adquisición de datos**: Se obtienen datos del sensor BNO055 conectados a Arduino DUE.
2. **Selección y procesamiento**: Se extraen los valores deseados y se convierten a formato `single`.
3. **Composición de la trama**: Los datos se estructuran en un formato de cadena de texto con separadores adecuados.
4. **Conversión a ASCII**: Se convierte la cadena a formato ASCII para su transmisión.
5. **Envío por puerto serie**: Se transmite la información a 115200 bps para su almacenamiento en un datalogger.

## Notas Adicionales
- Asegurarse de que el Arduino DUE esté correctamente conectado y reconocido por Simulink.
- Es recomendable validar la estructura de la trama en el datalogger para garantizar la correcta recepción de datos.

## Licencia
Este proyecto es de libre uso para propósitos educativos y de investigación. Creado por racarla96 (@racarla96), disponible en [https://github.com/racarla96/Arduino_Serial_Logger_Example](https://github.com/racarla96/Arduino_Serial_Logger_Example).

