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

