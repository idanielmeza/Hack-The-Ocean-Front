# HACK THE OCEAN - LAUNCHX
## Un proyecto de INNOVACCION VIRTUAL

Hack the Ocean es un hackathon con la iniciativa de implementar tecnologias de Frontend y Backend para explorar distintas problematicas, pensar en soluciones e implementarlas de manera que los conocimientos adquiridos por los Explorers tengan un aterrizaje al terreno practico y exploren nuevas soluciones a partir de su creatividad, conocimiento y objetivos a travez del trabajo en equipo.

## Woopas al Rescate 
Este proyecto apunta a crear consciencia de las distintas especies con a las que habitamos en el planeta, la situacion enla que se encuentran debido al cambio climatico, afectacion de su habitad, perdida de sus fuentes de alimento y la constante expansion del territorio humano.
Puedes vizualizar el proyecto aqui [Wooper al rescate](https://hacktheocean.azurewebsites.net/)

A traves de nuestra aplicacion podras vizualizar las distintas especies junto con informacion sobre ellas y podras filtrar por los distintos parametros:

```mermaid
flowchart TB
id1-->id2 & id7-->id3-->id5-->id4--Necesita ayuda-->id6-->id8--Que puedo hacer?-->id1
id4--No se encuentra en problemas-->id1
id8--Nuestra colaboracion-->id9

id1(Conoce a las especies)
id2([Donde se encuentran])
id3((Encontre una de ellas))
id4{Se encuentran en probemas?}
id5{{Hago una aportacion}}
id6[(Alamcenamos los datos para verificarlos)]
id7([Averigua sobre su situacion])
id8[[Ayudemoslas]]
id9(Notificaremos a las autoridades y grupos de proteccion y preservacion de la vida salvaje)
```


## Como funciona el proyecto
### Modelado de la API

```mermaid
classDiagram 
    class Especie
      Especie <|-- Estado  
      Especie <|-- Habitad  
      Especie <|-- Tipo
      Especie : +String nombre
      Especie : +String descripcion
      Especie : +String img
      Especie : +String descripcion
      Especie : +Int problematica
      Especie : +Schema Tipo
      Especie : +Schema Estado
      Especie : +Schema Habitad
        class Estado {
            +String Estado
        }
        class Habitad {
            +String Habitad
        }
        class Tipo {
            +String Tipo
        }
```
### Un form padrisimo!

```mermaid
classDiagram
    class Reporte
    Reporte : +String Titulo
    Reporte : +String Decripcion
    Reporte : +Date Fecha
    Reporte : +String Email
    Reporte : +String Ubicacion
    Reporte : +String Estado
    Reporte : +Boolean Finalizado
    Reporte : +Enviar Reporte()
```
### Cómo navego?
```mermaid
flowchart TB
id1-->id6-->id2-->id3--Filtros-->id4-->id5-->id7
id7--Juntos haremos crecer el proyecto-->id2
id4-->id6
id1(Mira la página)
id2(Aprendes)
id6(Está creciendo)
id3(Qué te interesa?)
id4(Aportas)
id5(A travez de un reporte)
id7(Una Api de las especies)
```

## Intrucciones para uso
Si el proyecto esta desplegado basta con ir al liink [Wooper al rescate](https://hacktheocean.azurewebsites.net/)

Para instalar las dependecias con el repositorio solo corre el comando:
>npm install

Ahora despliega la página de manera local
>npm run dev

Listo, ahora puedes dirigirte a la dirección local para ver el proyecto.