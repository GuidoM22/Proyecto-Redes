```mermaid
classDiagram
    class Libro {
        +String "El Eternauta"
        +String Dibujante(s): Francisco Solano López, Guionista(s): Héctor Germán Oesterheld, Historietas: Hora Cero Semanal
        +String isbn 9786077515739
        +boolean Disponible(Si)
    }

    class Miembros {
        +String Guido M
        +String 10
        +Retiro_Libro(El Eternauta)
        +Regreso_Libro(El Eternauta)
    }

    class Bibliotecario {
        +String Fulano
        +String 1
        +Agrega_Libro(El Eternauta)
        +Remover_Libro(El Eternauta)
    }

    class Libreria {
        +String Biblioteca
        +List 500493 Libros
        +List 49500 Miembros
        +List Fulano, Mengano
        +Agregar_miembro(Jose)
    }

    Library "1" -- "contains" Libro
    Library "1" -- "registers" Miembros
    Library "1" -- "manages" Libreria
