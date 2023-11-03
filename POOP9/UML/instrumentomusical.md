@startuml
scale 3

abstract class Object{

}

abstract class InstrumentoViento{

}

class Flauta{
    +tipoInstrumento():String
}

class InstrumentoMusical{
    +tocar():void
    +afinar():void
    +tipoInstrumento():String
}

Object<|-- InstrumentoViento
InstrumentoMusical<|-- InstrumentoViento: interfaz
InstrumentoViento<|-- Flauta
@enduml