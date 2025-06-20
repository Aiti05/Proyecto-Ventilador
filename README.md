## **Proyecto: Ventilador y Humidificador inteligentes**

## **1. Componentes:**
En este projecto estamos usando un total de nueve componentes diferentes:
1. ESP32-s3: Pieza principal del montaje donde irán conectados todos los componentes.
2. Ventilador: Componente base que se activa y apaga según lo programado
3. Sensor AHT10: Sensor I2C para captar temperatura y humedad.
4. Pantalla OLED: Pantalla donde proyectaremos la temperatura y la humedad que perciba el sensor. I2C
5. Relé: Utilizado para poder introducir más energía para el ventilador (12V) y el humidificador (5V).
6. Himudificador: Humidificador que pondremos sobre base de agua y a partir de ondas ultrasónicas.
7. LED's: Utilizados para avisar cuando se tiene que activar el humidificador y para cuando se activa el ventilador y asi verificar que no haya errores.
8. Pulsadores: Pulsadores para activar manualmente el  el ventilador y/o el humidificador.
9. Cables: Cables para realizar todas las conexiones entre el reto de componentes.


## **2. Presupuesto:**

## **3. Diagrama de bloques:**

```mermaid
graph LR

    %% Parte central: ESP32-S3 con "línea horizontal" simulada
    ESP32["Esp32 - S3<br>----------------------------------<br>Servidor web local"]

    %% Lado izquierdo (entradas)
    Sensor["Sensor Temperatura (I2C)"] --- ESP32
    LED_Aviso["LED (izquierdo) - Se tiene que encender humidificador"] --- Sensor

    %% Lado derecho (salidas)
    ESP32 --- Display["Display (Pantalla OLED)"]
    ESP32 --- Rele_Hum["Relé (Humidificador 5V)"]
    ESP32 --- Pulsador_Modo["Pulsador (Modo Auto / Modo Manual)"]
    ESP32 --- Pulsador_Activar["Pulsador (Para activar Ventilador)"]

    Pulsador_Activar --- Rele_Ventilador["Relé Ventilador 12V"]
    Pulsador_Activar --- LED_Ventilador["LED (derecho) - Ventilador encendido"]

    %% Flecha hacia abajo desde el ESP32
    ESP32 --> abajo[" web "]

```

## **4. Montaje:**
## **5. Funcionalidades:**
## **6. Conclusiones:**

**Codigo main.cpp:**
```


```
