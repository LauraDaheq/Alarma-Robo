# Alarma-Robo 🚨

Sistema de alarma anti-robo basado en Arduino con sensor ultrasónico HC-SR04.

## Descripción del Proyecto

Este proyecto implementa un sistema de alarma que detecta objetos o personas que se acercan a una distancia inferior a 10 cm usando un sensor ultrasónico. Cuando se detecta movimiento cerca, activa un zumbador que suena durante 5 segundos.

## Componentes Utilizados

- **Arduino UNO**: Microcontrolador principal
- **Sensor Ultrasónico HC-SR04**: Sensor de distancia (DIST1 en el esquema)
- **Zumbador (Buzzer)**: Emisor de sonido de alarma
- **Protoboard**: Para las conexiones
- **Jumpers**: Cables de conexión
- **Resistencias y condensadores**: Según sea necesario

## Pines Utilizados

| Componente | Pin Arduino |
|-----------|------------|
| TRIG (HC-SR04) | 7 |
| ECHO (HC-SR04) | 6 |
| Buzzer | 12 |

## Funcionamiento

1. El sensor ultrasónico emite un pulso de 5 microsegundos
2. Mide el tiempo que tarda en recibir el eco
3. Calcula la distancia usando la fórmula: `distancia = (duracion/2) * 0.0343 cm/μs`
4. Si la distancia es menor a 10 cm, activa el buzzer a 1000 Hz durante 5 segundos
5. Si la distancia es mayor, el buzzer permanece apagado

## Esquema de Conexión

Ver las imágenes incluidas en el repositorio para el diagrama de conexión detallado.

## Cómo Usar

1. Carga el código `ALARMAROBO.ino` en tu Arduino UNO
2. Realiza las conexiones según el esquema proporcionado
3. Alimenta el Arduino
4. El sistema comenzará a detectar objetos automáticamente
5. Cuando algo se acerque a menos de 10 cm, sonará la alarma

## Notas Importantes

- La velocidad del sonido utilizada es 343 m/s (a temperatura ambiente ~20°C)
- El sensor mide distancias de aproximadamente 2 cm a 4 metros
- El delay de 5 segundos durante la alarma puede ajustarse según necesidad
- La frecuencia del zumbador (1000 Hz) puede modificarse en el código
