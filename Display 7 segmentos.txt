void setup() {
  // Configuración de pines de entrada
  pinMode(2, INPUT); //A
  pinMode(3, INPUT); //B
  pinMode(4, INPUT); //C
  pinMode(5, INPUT); //D
  pinMode(6, INPUT); //E
  pinMode(7, INPUT); //F
  pinMode(8, INPUT); //G

  // Configuración de pines de salida
  pinMode(14, OUTPUT); //A
  pinMode(15, OUTPUT); //B
  pinMode(16, OUTPUT); //C
  pinMode(17, OUTPUT); //D
  pinMode(18, OUTPUT); //E
  pinMode(19, OUTPUT); //F
  pinMode(20, OUTPUT); //G
}

void loop() {
 
  int A = digitalRead(2);
  int B = digitalRead(3);
  int C = digitalRead(4);
  int D = digitalRead(5);
  int E = digitalRead(6);
  int F = digitalRead(7);
  int G = digitalRead(8);
   
  /*int A = LOW;
  int B = HIGH;
  int C = LOW;
  int D = LOW;
  int E = HIGH;
  int F = LOW;
  int G = LOW;
  */
  if (A & B & !C & D & E & F & G) {// (CERO)1101111
    digitalWrite(14, HIGH);
    digitalWrite(15, HIGH);
    digitalWrite(16, HIGH);
    digitalWrite(17, HIGH);
    digitalWrite(18, HIGH);
    digitalWrite(19, HIGH);
    digitalWrite(20, LOW);
  } else if (!A & B & !C & !D & E & !F & !G){// (UNO)0100100
    digitalWrite(14, LOW);
    digitalWrite(15, HIGH);
    digitalWrite(16, HIGH);
    digitalWrite(17, LOW);
    digitalWrite(18, LOW);
    digitalWrite(19, LOW);
    digitalWrite(20, LOW);
  }else if (A & B & C & !D & !E & F & G){// (DOS)1110011
    digitalWrite(14, HIGH);
    digitalWrite(15, HIGH);
    digitalWrite(16, LOW);
    digitalWrite(17, HIGH);
    digitalWrite(18, HIGH);
    digitalWrite(19, LOW);
    digitalWrite(20, HIGH);
  }else if ((A & B & C & !D & E & F & !G)){// (TRES) 1110110
    digitalWrite(14, HIGH);
    digitalWrite(15, HIGH);
    digitalWrite(16, HIGH);
    digitalWrite(17, HIGH);
    digitalWrite(18, LOW);
    digitalWrite(19, LOW);
    digitalWrite(20, HIGH);
  }else if ((!A & B & C & D & E & !F & !G)){// (CUATRO) 0111100
    digitalWrite(14, LOW);
    digitalWrite(15, HIGH);
    digitalWrite(16, HIGH);
    digitalWrite(17, LOW);
    digitalWrite(18, LOW);
    digitalWrite(19, HIGH);
    digitalWrite(20, HIGH);
  }else if ((A & !B & C & D & E & F & !G)){// (CINCO) 1011110
    digitalWrite(14, HIGH);
    digitalWrite(15, LOW);
    digitalWrite(16, HIGH);
    digitalWrite(17, HIGH);
    digitalWrite(18, LOW);
    digitalWrite(19, HIGH);
    digitalWrite(20, HIGH);
  }else if ((A & !B & C & D & E & F & G)){// (SEIS) 1011111
    digitalWrite(14, HIGH);
    digitalWrite(15, LOW);
    digitalWrite(16, HIGH);
    digitalWrite(17, HIGH);
    digitalWrite(18, HIGH);
    digitalWrite(19, HIGH);
    digitalWrite(20, HIGH);
  }else if ((A & B & !C & !D & E & !F & !G)){// (SIETE) 1100100
    digitalWrite(14, HIGH);
    digitalWrite(15, HIGH);
    digitalWrite(16, HIGH);
    digitalWrite(17, LOW);
    digitalWrite(18, LOW);
    digitalWrite(19, LOW);
    digitalWrite(20, LOW);
  }else if ((A & B & C & D & E & F & G)){// (OCHO) 1111111
    digitalWrite(14, HIGH);
    digitalWrite(15, HIGH);
    digitalWrite(16, HIGH);
    digitalWrite(17, HIGH);
    digitalWrite(18, HIGH);
    digitalWrite(19, HIGH);
    digitalWrite(20, HIGH);
  }else if ((A & B & C & D & E & !F & !G)){// (NUEVE) 1111100
    digitalWrite(14, HIGH);
    digitalWrite(15, HIGH);
    digitalWrite(16, HIGH);
    digitalWrite(17, LOW);
    digitalWrite(18, LOW);
    digitalWrite(19, HIGH);
    digitalWrite(20, HIGH);
  }else if ((A & B & C & D & E & !F & G)){// (A) 1111101
    digitalWrite(14, HIGH);
    digitalWrite(15, HIGH);
    digitalWrite(16, HIGH);
    digitalWrite(17, LOW);
    digitalWrite(18, HIGH);
    digitalWrite(19, HIGH);
    digitalWrite(20, HIGH);
  }else if ((!A & !B & C & D & E & F & G)){// (B) 0011111
    digitalWrite(14, LOW);
    digitalWrite(15, LOW);
    digitalWrite(16, HIGH);
    digitalWrite(17, HIGH);
    digitalWrite(18, HIGH);
    digitalWrite(19, HIGH);
    digitalWrite(20, HIGH);
  }else if ((A & !B & !C & D & !E & F & G)){// (C) 1001011
    digitalWrite(14, HIGH);
    digitalWrite(15, LOW);
    digitalWrite(16, LOW);
    digitalWrite(17, HIGH);
    digitalWrite(18, HIGH);
    digitalWrite(19, HIGH);
    digitalWrite(20, LOW);
  }else if ((!A & B & C & !D & E & F & G)){// (D) 0110111
    digitalWrite(14, LOW);
    digitalWrite(15, HIGH);
    digitalWrite(16, HIGH);
    digitalWrite(17, HIGH);
    digitalWrite(18, HIGH);
    digitalWrite(19, LOW);
    digitalWrite(20, HIGH);
  }else if ((A & !B & C & D & !E & F & G)){// (E) 1011011
    digitalWrite(14, HIGH);
    digitalWrite(15, LOW);
    digitalWrite(16, LOW);
    digitalWrite(17, HIGH);
    digitalWrite(18, HIGH);
    digitalWrite(19, HIGH);
    digitalWrite(20, HIGH);
  }else if ((A & !B & C & D & !E & !F & G)){// (F) 1011001
    digitalWrite(14, HIGH);
    digitalWrite(15, LOW);
    digitalWrite(16, LOW);
    digitalWrite(17, LOW);
    digitalWrite(18, HIGH);
    digitalWrite(19, HIGH);
    digitalWrite(20, HIGH);
  }else{
    digitalWrite(14, LOW);
    digitalWrite(15, LOW);
    digitalWrite(16, LOW);
    digitalWrite(17, LOW);
    digitalWrite(18, LOW);
    digitalWrite(19, LOW);
    digitalWrite(20, LOW);
  }
}