# Gustos

Unos amigos se están por abrir un bilichito y nos pidieron un sistema para determinar qué cosas le gustan a las personas. Nos dieron [esta documentación](doc/objetosGustos.md) que indica qué cosas esperan del sistema.

Por suerte para nosotros, alguien ya implementó lo pedido. Pero nos dieron la tarea de **revisar** el trabajo.

## Code Review

Revisar que lo que esté hecho funciona correctamente. Para ello se cuenta con algunos tests que prueban la funcionalidad de algunos objetos. Correrlos y ver que todo esté correcto y sin errores.

**En el caso de encontrar errores deberán arreglarlos** teniendo la documentación otorgada como _fuente de la verdad_.

## Más cosas

Agregar al modelo estos objetos:

- un _arito_ celeste de cobre, que pesa 180 gramos.
- un _banquito_ de madera que pesa 1700 gramos. 
  Al principio es naranja, pero puede cambiar de color. 
  El naranja es un color fuerte.
- una _cajita_ roja, que tiene un objeto adentro. La cajita puede ser de cualquier material. 
  Este objeto puede ser cualquiera de los definidos previamente, y puede cambiar.
  El peso de la cajita es de 400 gramos más el peso de lo que tiene adentro.
    
Y tener tests que prueben los siguientes casos:
- Un bolichito con un banquito en mostrador y una cajita de cobre con una pelota dentro en vidriera no está desequilibrado y tiene algo naranja.
- El caso anterior pero si en vez de la pelota hay un arito dentro de la cajita, entonces sí está desequilibrado.
- El caso anterior pero si se le cambia el color del banquito por verde, entonces deja de tener algo naranja.


## Se hizo la luz

Además nos piden saber si **el bolichito tiene luz** que se cumple cuando alguno de los dos objetos está hecho de un material que conduce la electricidad. 

De los materiales que tenemos por ahora: el cobre conduce la electricidad siempre, y del plomo sabemos que conduce la electricidad cuando la _resistividad_ es menor a `0.5`. La _resistividad_ del plomo depende de su estado:
  - Cuando está al natural, el material brilla y su resistividad es de `0.7`.
  - Cuando está oxidado, el material no brilla y su resistividad es de `1`.
  - Cuando está cromado, el material brilla y su resistividad es de `0.2`.

Testear los siguientes casos de prueba:
  - Un bolichito con un muñeco de 500 gramos en mostrador y una cajita de plomo con un arito dentro en vidriera es brillante pero no tiene luz.
  - La misma situación pero con una cajita de plomo cromado, entonces el bolichito es brillante y tiene luz.
  - La misma situación pero con una cajita de plomo oxidado, entonces el bolichito no es brillante ni tiene luz.
