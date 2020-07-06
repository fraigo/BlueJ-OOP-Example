La interfaz es una herramienta útil para definir un conjunto de funcionalidades abstractas y comunes de algunas entidades genéricas 

Ejemplo: un aparato electrónico

interface ElectronicDevice {
	public void on();
	public void off();
    
}


Luego puede definirse una interfaz que extiende la anterior

interface Television extends ElectronicDevice {
	
	public void setChannel(int channel);
	public void setVolume(int volume);
}


Luego una clase puede implementar la interfaz

class MyTelevision implements Television{
 public void on(){
     //codigo para encender
 }
 public void off(){
     // codigo para apagar
 }
 public void setChannel(int ch){
     // codigo para cambiar al canal ch
 }
 public void setVolume(int vol){
     // codigo para establecer volumen vol
 }
}


Y otra clase puede extender la clase base (hereda los métodos anteriores):

class MySmartTelevision extends MyTelevision {
 public void launchApp(int appId){
     // codigo para abrir aplicacion appId
 }
 public void closeApp(int appId){
     // codigo para cerrar aplicacion appId
 }
}

