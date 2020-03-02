```mermaid

classDiagram

      Avión "1" <|-- "0..*" Vuelo : es realizado
      Vuelo "0..*" <|-- "0..*" Persona : pasajero 
      Billete .. Vuelo
      Billete .. Persona

      class Vuelo{
         -fecha : Date
         -plazas : Integer
      }

      class Avión{
         -modelo : String
         -capacidad : Integer
      }

      class Persona{
         -nombre : String
         -apellidos : String
         -edad : Date
         -sexo : Genero
        }

      class Genero{
         <<enumeration>>
         Hombre
         Mujer
      }

      class Billete{
         -asiento : Integer
      }