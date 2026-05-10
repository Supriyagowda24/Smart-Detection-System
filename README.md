PIR Motion Detection System using Arduino UNO

📌 Overview:

This project demonstrates a simple Motion Detection System using an Arduino UNO, PIR Sensor, and LED.
The PIR sensor detects movement and sends a HIGH signal to the Arduino. Based on this signal, the Arduino turns ON the LED and displays the motion status on the Serial Monitor.

This project is useful for learning:
Arduino programming
PIR sensor interfacing
Embedded systems basics
Home automation concepts

🛠 Components Required:

Arduino UNO	
PIR Sensor	
LED	
220Ω Resistor	
Breadboard	
Jumper Wires	
USB Cable	

🔌 Circuit Connections

PIR Sensor to Arduino:

PIR Sensor	Arduino UNO
VCC	        5V
GND	        GND
OUT	        D2

LED Connections:
LED Pin      	Arduino Connection
Positive (+)	D13 through 220Ω resistor
Negative (-)	GND

⚙️ Working Principle:

The PIR sensor monitors infrared radiation.
When motion is detected, the PIR output becomes HIGH.
Arduino reads the HIGH signal from pin D2.
The LED connected to pin D13 turns ON.
Serial Monitor displays:
“Motion Detected!”
When no motion is detected:
LED turns OFF
Serial Monitor displays “No Motion”

💻 Arduino Code

```cpp
int pirPin = 2;
int ledPin = 13;

void setup() {

  pinMode(pirPin, INPUT);
  pinMode(ledPin, OUTPUT);

  Serial.begin(9600);

  Serial.println("PIR Motion Sensor Started");
}

void loop() {

  int motion = digitalRead(pirPin);

  if (motion == HIGH) {

    digitalWrite(ledPin, HIGH);

    Serial.println("Motion Detected!");

  }
  else {

    digitalWrite(ledPin, LOW);

    Serial.println("No Motion");

  }

  delay(200);
}

```

📊 Output:

Motion Status	LED	Serial Monitor.

Motion Detected	ON	Motion Detected!

No Motion	OFF	No Motion.

✅ Conclusion

This project successfully demonstrates a basic motion detection and alert system using Arduino UNO and a PIR sensor. It helps beginners understand sensor interfacing, digital input/output operations, and embedded system applications in real-world automation systems.
