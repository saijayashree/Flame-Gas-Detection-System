# Flame-Gas-Detection-System
Arduino project for flame and gas detection using sensors, buzzer, and LEDs.



## Components
- Arduino Uno
- MQ2 Gas Sensor
- Flame Sensor
- Buzzers (2)
- LEDs (Red x2, Green x1)

## Working
- Gas + Flame → Both buzzers ON, both red LEDs ON, green LED OFF  
- Gas only → Buzzer1 ON, Red LED1 ON  
- Flame only → Buzzer2 ON, Red LED2 ON  
- Safe → Buzzers OFF, red LEDs OFF, green LED ON  

## Code Preview
```cpp
int redLed1 = 3;
int redLed2 = 4;
int greenLed = 8;
int buzzer1 = 5;
int buzzer2 = 6;
int gasPin = A0;
int flamePin = 2;
int gasSensorThres = 400;

void setup() {
  pinMode(redLed1, OUTPUT);
  pinMode(redLed2, OUTPUT);
  pinMode(greenLed, OUTPUT);
  pinMode(buzzer1, OUTPUT);
  pinMode(buzzer2, OUTPUT);
  pinMode(gasPin, INPUT);
  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() {
  int gasSensor = analogRead(gasPin);
  int flameSensor = digitalRead(flamePin);
  // logic here...
}
