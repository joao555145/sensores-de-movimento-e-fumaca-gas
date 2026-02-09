/* Programa: Detector de gás e fumaça */

/* Definição dos pinos */
#define MQ_analogico A0
#define MQ_digital 4
#define Buzzer 5
#define Led_Verde 6
#define Led_Vermelho 7

/* Variáveis */
int valor_analogico;
int valor_digital;

void setup() {
  Serial.begin(9600);

  pinMode(MQ_analogico, INPUT);
  pinMode(MQ_digital, INPUT);
  pinMode(Buzzer, OUTPUT);
  pinMode(Led_Verde, OUTPUT);
  pinMode(Led_Vermelho, OUTPUT);

  digitalWrite(Led_Verde, HIGH);   // começa seguro
  digitalWrite(Led_Vermelho, LOW);
  noTone(Buzzer);
}

void loop() {
  valor_analogico = analogRead(MQ_analogico);
  valor_digital = digitalRead(MQ_digital);

  Serial.print("Nível detectado : ");
  Serial.print(valor_analogico);
  Serial.print(" || ");

  if (valor_analogico > 70) {
    digitalWrite(Led_Vermelho, HIGH);
    digitalWrite(Led_Verde, LOW);
    tone(Buzzer, 1000);
    Serial.println("⚠️  GÁS DETECTADO!");
  } else {
    digitalWrite(Led_Vermelho, LOW);
    digitalWrite(Led_Verde, HIGH);
    noTone(Buzzer);
    Serial.println("✅ Ambiente Seguro.");
  }

  delay(200);
}