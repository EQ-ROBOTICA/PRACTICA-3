# PRACTICA-3

# Integrantes:
 - Edgar Zahid Hernandez Garcia
 - Gael Mateo Rangel Chavez
 - Alejandro Saldaña Garcia

# Introducción
La robótica industrial es un sector en constante crecimiento y evolución. Actualmente, los robots realizan una amplia variedad de tareas que antes eran ejecutadas por humanos, como ensamblar productos (vehículos, electrodomésticos, dispositivos), realizar cirugías, pintar piezas, entre otras. Estas capacidades se logran, en parte, gracias a la programación, que permite asignar instrucciones específicas para llevar a cabo acciones determinadas.
En esta práctica, el objetivo es implementar un código que permita controlar un brazo robótico Epson C4, logrando que se mueva, agarre un objeto y lo deposite en un lugar específico.

# Instrucciones
- Programación de coordenadas
  
  Para asegurar que el robot se desplace sin riesgo de colisión, se implementó un sistema de movimientos manuales utilizando el software EpsonRC+.
  A través de este software, se definió el punto de inicio o "Home" y las demás coordenadas necesarias para su movimiento.

  En nuestro caso, empleamos tres puntos: "Primera", "Segunda", "Tercera", "Cuarta" y "Caja". Cada uno de estos puntos fue almacenado con su respectivo nombre a medida que 
  íbamos moviendo el robot, creando así una trayectoria de tres puntos que luego se ejecutaría mediante código.

- Programación final mediante código
  
  Para implementar la lógica del movimiento según las coordenadas definidas, se accedió a la ventana "Main" del software y se escribió el siguiente código:

```
Function main
Home
Go Primera
Go Segunda
Off 2
Go Primera
Go Caja
On 2
Home
Go Tercera
Go Cuarta
Off 2
Go Tercera
Go Primera
Go Segunda
On 2
Go Primera
Home
Go Caja
Off 2
Go Tercera
Go Cuarta
On 2
Go Tercera
Home
Fend
```
Se estableció el punto de inicio "Home" y, mediante el comando Go, se indicó al robot que se desplazara al primer punto y, a continuación, al segundo. Al llegar al segundo punto, el brazo robótico ya se encontraba sobre el objeto, por lo que con el comando Off y el valor 2 (predefinido para la garra) se cerró la garra y se tomó el objeto. Seguidamente, se le ordenó regresar al primer punto para asegurar un movimiento seguro, y después se dirigió al punto caja, donde se encontraba el lugar de destino soltando el objeto con Off 2. Una vez allí, el comando On 2 permitió abrir la garra y soltar el objeto. Regresa al punto Home para no tener una colisión, se mueve al tercer punto para después llegar a la cuarta posición para agarrar la pieza con el comando On 2, regresa a la Tercera posición, pasa a la primera finalizando en segunda posición para tomar el objeto con On 2, regresa a la primera posición, a su punto Home para de ahí tomar el objeto en caja On 2, llevando a Tercera y cuarta posición para soltar con off 2 el objeto dando finalizado el código.
# CONCLUSIONES:
-Alejandro Saldaña García: En conclusión, en la práctica se realizó el código de la forma más eficiente y rápida posible, utilizando de forma múltiple los puntos asignados que programamos en el robot para no realizar movimientos ni colisiones durante la reproducción del movimiento.

-Gael Mateo Rangel Chávez: Esta práctica demuestra la importancia de la programación en la róbotica industrial para realizar tareas precisas. Este ejercicio refleja como la róbotica puede optimizar distintos procesos industriales, reduciendo tiempos y aumentando la precisión.

-Edgar Zahid Hernandez García: La práctica me permitió comprender con mayor claridad cómo se aplica la robótica para llevar a cabo tareas específicas. Considero que su implementación es altamente efectiva y ofrece una gran utilidad. En esta ocasión, la tarea fue un poco mas laboriosa que la practica 1 aunque misma doficultad, pero imagino que para procesos industriales, la complejidad del código necesario aumentará considerablemente.


