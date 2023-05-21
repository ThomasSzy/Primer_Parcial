#Primer Parcial

![LOGO TINKERCAD](https://i.ibb.co/K08W9N9/Arduino-Tinkercad.jpg)

## Nombre y Apellido:
* Thomas Szymuda


## Primer Parcial Imagen

![IMAGEN DEL PROYECTO](https://i.im.ge/2023/05/21/hrXklq.Thomas-Szymuda-Primer-Parcial-1D.png)

## DESCRIPCIÓN

Este parcial trata sobre un acensor en el cual informa en el piso que estamos, si esta parado o no con unos les y sus tres botones cada uno es para subir, bajar y parar el acensor

## FUNCIÓN PRINCIPAL

La función principal se encarga de elevar, parar y subir el acensor <br/>
Tambien tiene unos leds los cuales dicen el estado de funcionamiento del acensor  <br/>
//Thomas Szymuda 1D
//Primer Parcial
void loop()
{
  //Botones
  int boton_sube;
  boton_sube = digitalRead(BOTON_SUBIR);
  int boton_bajar;
  boton_bajar = digitalRead(BOTON_BAJAR); 
  
  int boton_pausar;
  boton_pausar = digitalRead(BOTON_PARAR);
  
  //piso
  Serial.print("Piso: ");    
  Serial.println(numero_piso);
  //Encendido
  encender_piso(numero_piso);
  //ESTADO ACENSOR
  estado_acensor(boton_pausar, boton_sube, boton_bajar, 0, 9);
  //Delay y estado de leds
  leds_estado_acensor();
}


## LINK AL PROYECTO

* [proyecto](https://www.tinkercad.com/things/aKWD3EvCdZf-thomas-szymuda-primer-parcial-1d/editel?sharecode=MlZMHsljp4uCzf2Ox6tsOUdIE9h367a8QeluCDKRAsY)
