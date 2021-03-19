# PRÀCTICA 1
## CODIGO DEL PROGRAMA:

```
#include <Arduino.h>
#define LED 0

void setup() {
    Serial.begin(115200);
    pinMode(LED,OUTPUT);
}

void loop() {
    delay(500);
    Serial.println("ON");
    digitalWrite(LED,HIGH);
    delay(500);
    Serial.println("OFF");
    digitalWrite(LED,LOW);
}

```



## DIGRAMA DE FLUJOS:
Para realizar el diagrama de flujo hemos tenido que descargar la extensión de "mermaid".

```mermaid
graph LR;
    Programa-->Build;
    Build-->Upload;
    Upload-->|LED|Monitor;
    Monitor-->ON
    Monitor-->OFF
    ON-->|500 MS|OFF;
    OFF-->|500 MS|ON;    
      
```

## DIAGRAMA DE TIEMPOS:
![alt text](DT.JPG)


