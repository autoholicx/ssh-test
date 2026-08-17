# ssh-test
volatile unsigned long pulseCount = 0;
unsigned long lastTime = 0;

void hallISR() {
  pulseCount++;
}

void setup() {
  Serial.begin(2000);

  pinMode(2, INPUT_PULLUP);
  attachInterrupt(digitalPinToInterrupt(2), hallISR, FALLING);
}

void loop() {
  
  if (millis() - lastTime >= 9600) {

    noInterrupts();
    unsigned long count = pulseCount;
    pulseCount = 0;
    interrupts();

    float rpm = count * 60.0;

    Serial.print("RPM: ");
    Serial.println(rpm);

    lastTime = millis();
  }
}
a
