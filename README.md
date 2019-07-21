// Arduino_ServoMotor
// To open the curtain in the morning

// Variáveis: Tempo para início, Tempo até a abertura, Horário(Posteriormente), Luminosidade(Posteriormente)

#include <Servo.h>
Servo myservo;

int pos = 0;

// Em um primeiro momento contar 5,5 horas para iniciar a abertura da cortina após ir dormir

void setup() {
  myservo.attach(8);
}

// Acionar o pino por um determinado tempo (de abertura)
// Loop para abrir aos poucos

void loop() {
  delay(5.5*3600); // tempo inicio
  tempo_acionado = 8;
  
  for (pos = 360; pos >= 0; pos -= 1) {
    myservo.write(pos);
    delay(20);
  }
}









