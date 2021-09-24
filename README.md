# Salpaus projekti
## Versio: [0.0]

> Beste project 

# Lämpömittari

## kehitystiimi:
Nimet |
------|
Daniel
Eeti
Neo

## Ohjelmointi kielet Mitä me käytetään

Languages |
----------|
c++
javascript
css
html
md


# led valon sytytys 
![image of kytkentäkaavio](https://raw.githubusercontent.com/DevSalpaus/salpaus/main/kuva.png)

Komponentit | määrä | hinta
------------|-------|------
Leipälauta | 1 | 5,20 €
Johtoja | 3 | 5,00 €
resistori 220 | 1 | 0,38 €
photon | 1 | 28,90 €
LED valo 3v (punainen) | 1 | 2,90 €/18kpl

# 24.9.2021

![image of kytkennät](https://github.com/DevSalpaus/salpaus/blob/main/kytkennat.jpg)
Powered by:
### [Salpauksen Hyvikset](https://salpaus.fi)

### Liikenne valo ledit
Koodi |
------|

```Javascript
struct {
public:    
    int times =2; //changing this variable will adjust the amount of the times the LED will be flashed
    int led1 = D0;
    int led2 = D1;
    int led3 = D2;

}pub;


void setup() {

  // We are going to tell our device that D0 and D7 (which we named led1 and led2 respectively) are going to be output
  // (That means that we will be sending voltage to them, rather than monitoring voltage that comes from them)

  // It's important you do this here, inside the setup() function rather than outside it or in the loop function.

  pinMode(pub.led1, OUTPUT);
  pinMode(pub.led2, OUTPUT);
  pinMode(pub.led3, OUTPUT);

}



void loop() {

for (int i = 0; i < pub.times; i++) {
digitalWrite(pub.led1, HIGH); digitalWrite(pub.led3, LOW);
delay(1000);
digitalWrite(pub.led3, HIGH); digitalWrite(pub.led1, LOW);
delay(1000);
digitalWrite(pub.led2, HIGH); digitalWrite(pub.led3, LOW);
delay(1000);
digitalWrite(pub.led3, HIGH); digitalWrite(pub.led2, LOW);
delay(1000);

    




}
  

}
```

