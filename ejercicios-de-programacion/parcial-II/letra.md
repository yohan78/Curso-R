Parcial II
==========

#### Curso IMSER 2012

Instrucciones:
--------------

Instrucciones:
En el archivo "parcial-II.R" ud. tiene un script en el cual deberá guardar todos los comandos del ejercicio, siguiendo la demarcación que se muestra en el mismo.

Nota: los ejercicios del parcial son dependientes de los anteriores en el sentido de que utilizan objetos creados, pero no implica que no se puedan tratar de resolver independientemente.

Los ejercicios con (``*``) presentan un puntaje de 1.5, mientras que los que no tienen (``*``) equivalen a 1 punto.

Una vez terminado el parcial usted deberá subir a la página del EVA el archivo “parcial-II.R”.




Para simular la cantidad de pasajeros de un ómnibus urbano se ha creado el código que aparece sobre el final del ejercicio (y que también se encuentra en el script parcial-II.R). El criterio es el siguiente: el bus recorre 25 paradas, empezando el trayecto sin pasajeros. En cada parada se subirán de 0 a 6 personas, pero debido a que existe un máximo estipulado de personas, a partir del momento en que se alcanza el total de 44 pasajeros el vehículo deja de parar.

#### (``*``) a.

Completar el código: las líneas en blanco que se encuentran dentro de los límites del código indican en dónde debe cambiarse. **El resto de las líneas están correctas**.

#### b.

Modifique el código de la parte anterior de forma tal que haga lo mismo, pero utilizando un loop ``while``.

#### (``*``) c.

Modifique el código reparado en la parte **a** para crear una función que ejecute la misma simulación, en la que el número de paradas y capacidad máxima del bus sean los argumentos de la misma. 

#### d.

Hacer una variante del código (de cualquiera de las partes anteriores) en la que además de subir personas, a partir de la parada 10 se bajen entre 0 y 4 pasajeros por parada.

Código fuente:


```r
paradas <- 25
pasajeros <- 0

registro[1] <- pasajeros
for (i in 1:paradas) {

  if (pasajeros >= 44) {

    registro[i:paradas] <- 44
    cat('Bus lleno!\n')
    break

  registro[i] <- pasajeros
  cat('Parada', i, 'hay', pasajeros, 'pasajeros\n')
}
plot(registro, xlab='Parada', ylab='No. de pasajeros')
```

