# trabajo  Arquitectura de Hardware 5º
#practic 30,04,21
// Realizar un programa que muestre cada 1 segundo el tiempo transcurrido desde que se encendió el arduino. (este si puede usar la función delay ())
// codigo 


unsigned long tiempo1 = 0;
unsigned long tiempo2 = 0;
unsigned long tiempoSegundos = 0;
 
configuración vacía () {
Serial.begin (9600);
tiempo1 = milis ();
 
}
 
bucle vacío () {
 
tiempo2 = milis ();

if (tiempo2> (tiempo1 + 1000)) {// Si ha pasado 1 segundo ejecuta el IF
tiempo1 = milis (); // Actualiza el tiempo actual
tiempoSegundos = tiempo1 / 1000;
Serial.print ("Ha transcurrido:");
Serial.print (tiempoSegundos);
Serial.println ("desde que se encendio el Arduino");
} 



// Realizar un programa que muestre cada 2 segundos el mensaje "Timer activado".
// codigo 

temporizador int largo = 2000;
unsigned long tiempo1 = 0;
unsigned long tiempo2 = 0;
unsigned long tiempoSegundos = 0;
 
configuración vacía () {
Serial.begin (9600);
tiempo1 = milis ();
 
}
 
bucle vacío () {
 
tiempo2 = milis ();
if (tiempo2> (tiempo1 + 2000)) {
tiempo1 = milis ();
tiempoSegundos = tiempo1 / 1000;
Serial.println ("TEMPORIZADOR ACTIVADO");

}
 
}

// Realizar un programa que cada dos segundos prenda o apague un LED.
// codigo

temporizador int largo = 2000;
unsigned long tiempo1 = 0;
unsigned long tiempo2 = 0;
int ledPin1 = 3;
 
configuración vacía () {
Serial.begin (9600);
pinMode (ledPin1, SALIDA);
 
}
 
bucle vacío () {
 
tiempo1 = milis ();
if ((tiempo1 - tiempo2)> 2000) {
digitalWrite (ledPin1, ALTO);
if ((tiempo1 - tiempo2)> 4000) {
digitalWrite (ledPin1, BAJO);
tiempo2 = tiempo1;
}
}
}
// Realizar un programa donde se conecten dos LEDs, el uno parpadee cada 2 segundos y el otro cada 1 segundo.
// codigo

temporizador int largo = 2000;

unsigned long tiempo1 = 0;

unsigned long tiempo2 = 0;

int ledPin1 = 3;

int ledPin2 = 4;

 

configuración vacía () {

Serial.begin (9600);

pinMode (ledPin1, SALIDA);

pinMode (ledPin2, SALIDA);

 

}

 

bucle vacío () {

 

tiempo1 = milis ();

if ((tiempo1 - tiempo2)> 2000) {

digitalWrite (ledPin1, ALTO);

if ((tiempo1 - tiempo2)> 4000) {

digitalWrite (ledPin1, BAJO);

tiempo2 = tiempo1;

}

}

if ((tiempo1 - tiempo2)> 1000) {

digitalWrite (ledPin2, ALTO);

if ((tiempo1 - tiempo2)> 2000) {

digitalWrite (ledPin2, BAJO);

tiempo2 = tiempo1;

}

}

}


// Realizar el ejercicio del semáforo explicado en la primera actividad utilizando temporizadores.
// codigo

int ledRojo = 4;

int ledAmarillo = 2;

int ledVerde = 3;

 

unsigned long tiempo1 = 0;

unsigned long tiempo2 = 0;

 

 

 

configuración vacía ()

{

Serial.begin (9600);

pinMode (ledRojo, SALIDA);

pinMode (ledAmarillo, SALIDA);

pinMode (ledVerde, SALIDA);

}

 

bucle vacío ()

{

tiempo1 = milis ();

if ((tiempo1-tiempo2)> 2000) {

digitalWrite (ledRojo, ALTO);

digitalWrite (ledAmarillo, BAJO);

digitalWrite (ledVerde, BAJO);

 

if ((tiempo1-tiempo2)> 3000) {

digitalWrite (ledRojo, BAJO);

digitalWrite (ledAmarillo, ALTO);

digitalWrite (ledVerde, BAJO);

if ((tiempo1 - tiempo2)> 4000) {

digitalWrite (ledRojo, BAJO);

digitalWrite (ledAmarillo, BAJO);

digitalWrite (ledVerde, ALTO);

tiempo2 = tiempo1;

}

}

}

 

}



