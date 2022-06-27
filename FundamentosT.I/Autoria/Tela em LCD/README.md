# Autoria Rodrigo Xavier
## Descrição 
Autoria feita em arduino no dia 20 de junho.
## Imagem de funcionamento.
A cada dois segundos a tela LCD se reinicia.

![image](https://user-images.githubusercontent.com/102531891/175958215-95123599-2162-4be4-9bad-6c176ba6cc8e.png)


![image](https://user-images.githubusercontent.com/102531891/175957223-de86d2c1-4c13-456f-8392-9306ea03e18d.png)

## Código 
//Programa: Display LCD 16x2 e modulo I2C
//Autor: Arduino e Cia
#include <Wire.h>
#include <LiquidCrystal_I2C.h>
//Inicializa o display no endereco 0x27
LiquidCrystal_I2C lcd(0x27,16,2);
 
void setup()
{
 lcd.init();
}
 
void loop()
{
  lcd.setBacklight(HIGH);
  lcd.setCursor(0,0);
  lcd.print("Arduino e Cia !!");
  lcd.setCursor(0,1);
  lcd.print("LCD e modulo I2C");
  delay(1000);
  lcd.setBacklight(LOW);
  delay(1000);
}
