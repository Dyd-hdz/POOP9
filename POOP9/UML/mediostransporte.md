@startuml
scale 3

class MediosTransporte{
    -tam:String
    -color:String
    -peso:float
    +avanzar():void
    +encender():void
    +apagar():void
}

class TransporteAcuatico{
    -velocidad:int
    -capacidad:String
    -direccion:String
    +aumentarVelocidad():void
    +trasladar():void
    +frenar():void
}

class Barco{
    -puertoOrigen:String
    -puertoDestino:String
    -nPasajeros:int
    +abordadPasajeros():void
    +navegar():void
    +alertar():void
}

class Trajinera{
    -nPasajeros:int
    -nTrajineros:int
    -tiempo:float
    +detener():void
    +girar(String lado):void
    +remar():void
}

class TransporteAereo{
    -direccion:String
    -lugarOrigen:String
    -duracionViaje:float
    +volar():void
    +descender():void
    +altitud():void
}

class Avion{
    -aereolina:String
    -nPasajeros:int
    -nPersonal:int
    +volar():void
    +disminuirVel():void
    +acelelar():void
}

class Helicoptero{
    -nHelices:int
    -nPasajeros:int
    -modelo:int
    +girarHelices():void
    +ascender():void
    descender():void
}

class TransporteTerrestre{
    -direccion:Strig
    -lugarOrigen:String
    -duracionViaje:float
    +encender():void
    +apagar():void
    +msj():void
}

class Subterraneo{
    -combustible:String
    -ruta:String
    -llantaRiel:String
    +parar():void
    +luces():void
    +mensaje(String estacion):void
}

class Supraterraneo{
    -combustible:String
    -ruta:String
    -nllanta:int
    +cargarCombustible():void
    +luces():void
    +girar():void
}

class Metro{
    -nPasajeros:int
    -nVagones:int
    -nEstaciones:int
    +girar():void
    +emergencia():void
    +abrirPuertas():void
}

class Suburbano{
    -nPasajeros:int
    -nVagones:int
    -vel:float
    +abrirPuertas():void
    +llegar(String estacion):void
    +sonar(String estacion):void
}

class Taxi{
    -modelo:int
    -nPuertas:int
    -placa:String
    +frenar():void
    +acelelar():void
    +radio():void
}

class Combi{
    -placa:String
    -nPasajeros:int
    -modelo:int
    +cerrarPuerta():void
    +frenar():void
    +recibirPago(float pago):void
}


MediosTransporte<|-- TransporteAcuatico
MediosTransporte<|-- TransporteAereo
MediosTransporte<|-- TransporteTerrestre
TransporteAcuatico<|-- Barco
TransporteAcuatico<|-- Trajinera
TransporteAereo<|-- Avion
TransporteAereo<|-- Helicoptero
TransporteTerrestre<|-- Subterraneo
TransporteTerrestre<|-- Supraterraneo
Subterraneo<|-- Metro
Subterraneo<|-- Suburbano
Supraterraneo<|-- Taxi
Supraterraneo<|-- Combi

@enduml