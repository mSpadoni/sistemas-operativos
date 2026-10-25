# C-Comenta: sistema operativo distribuido en C

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Sockets TCP](https://img.shields.io/badge/Sockets-TCP-555?style=flat-square)
![Threads](https://img.shields.io/badge/Multithreading-pthreads-555?style=flat-square)

Trabajo práctico de Sistemas Operativos (UTN-FRBA, 2024), hecho en un equipo de 5. Construimos en **C sobre Linux** una simulación de un sistema operativo dividida en cuatro programas independientes, que pueden correr en computadoras distintas y se comunican por **sockets TCP** con un protocolo de mensajes propio:
- el **Kernel** crea procesos y los planifica con FIFO, Round Robin y Virtual Round Robin;
- la **CPU** ejecuta sus instrucciones y traduce direcciones con una MMU y una TLB;
- la **Memoria** guarda los datos de cada proceso usando paginación;
- las **interfaces de entrada/salida** simulan dispositivos y un sistema de archivos propio.

Todo funciona en paralelo con **hilos y semáforos**, y deja logs que permiten seguir cada paso. **Yo desarrollé el módulo de Memoria**: tablas de páginas, asignación y liberación de marcos, procesos que crecen o se achican en tiempo de ejecución (con error de memoria llena), y lecturas y escrituras que pueden ocupar varias páginas. También colaboré en la CPU.

<details>
<summary>Cómo compilar</summary>

Requiere la [so-commons-library](https://github.com/sisoputnfrba/so-commons-library). Después, en cada módulo (`kernel`, `cpu`, `memoria`, `entradasalida`), ejecutá `make`. El ejecutable queda en `bin/` y se configura con su archivo `.config`.
</details>
