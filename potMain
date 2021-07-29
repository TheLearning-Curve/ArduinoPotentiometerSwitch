//@TheLearning-Curve, Please Subscribe on Youtube for more videos!


int potPin = A0; //What pin the Potentiometer Sensor is plugged into
int in1 = 12; //What pin the relay is plugged into

int val = 0;  //Creating a data storage point for the Sensor

int threshMin = 200;  //What is the Min reading you want to use to activate the relay
int threshMax = 300;  //What is the Max reading you want to use to activate the relay


void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600); //What is the port your Serial Monitor is in? 9600 is standard
  pinMode(in1, OUTPUT); //We are sending a signal to the realy board
  digitalWrite(in1,LOW);  //The signal we send to the relay will start off as LOW (off)

}

void loop() {
  // put your main code here, to run repeatedly:
  
  val = analogRead(potPin); //Set the val variable = the sensor readings

  if ((val >= threshMin) && (val <= threshMax)) {
    digitalWrite(in1, HIGH);  //If the sensor is between those values, turn the relay on
  } else {
    digitalWrite(in1, LOW); //...otherwise keep it off or turn it off
  }
//monitor(); //Uncomment to find your values you want to use
}

void monitor() {
  Serial.println("Potentiometer Reading: ")
  Serial.println(val);
  //delay(1000);  //Uncomment for slower readings in your Serial Monitor
}
