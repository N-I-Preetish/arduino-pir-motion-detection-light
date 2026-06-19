# Arduino PIR Motion Detection Light

## Project Overview

This project uses an Arduino Uno and a PIR (Passive Infrared) Motion Sensor to detect human movement. When motion is detected, an LED turns ON automatically and remains ON for a specified duration.

## Components Used

* Arduino Uno
* HC-SR501 PIR Motion Sensor
* LED
* 220Ω Resistor
* Breadboard
* Jumper Wires
* USB Cable

## Circuit Connections

### PIR Sensor

| PIR Sensor Pin | Arduino Uno   |
| -------------- | ------------- |
| VCC            | 5V            |
| GND            | GND           |
| OUT            | Digital Pin 2 |

### LED

| LED Connection   | Arduino Uno                  |
| ---------------- | ---------------------------- |
| Positive Leg (+) | Pin 13 through 220Ω Resistor |
| Negative Leg (-) | GND                          |

## Arduino Code

```cpp
int pirPin = 2;
int ledPin = 13;

void setup() {
  pinMode(pirPin, INPUT);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  if (digitalRead(pirPin) == HIGH) {
    digitalWrite(ledPin, HIGH);
    delay(5000);
  }
  else {
    digitalWrite(ledPin, LOW);
  }
}
```

## Working Principle

1. The PIR sensor detects motion.
2. The Arduino reads the sensor output.
3. When motion is detected, the LED turns ON.
4. The LED remains ON for 5 seconds.
5. If no motion is detected, the LED turns OFF.

## Applications

* Automatic Room Lighting
* Smart Home Systems
* Energy Saving Systems
* Security Monitoring

## Author

N. I. Preetish
First Year ECE
Velammal Engineering College
Project Date: June 2026
