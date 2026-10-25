# C-Comenta: sistema operativo distribuido en C

**Simulación de un sistema operativo** con 4 módulos que corren por separado y se comunican por red. TP de Sistemas Operativos (UTN-FRBA, 2024), en un equipo de 5.

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Sockets TCP](https://img.shields.io/badge/Sockets-TCP-555?style=flat-square)
![Threads](https://img.shields.io/badge/Multithreading-pthreads-555?style=flat-square)

- **Kernel:** planifica procesos con FIFO, Round Robin y Virtual Round Robin.
- **CPU:** ejecuta instrucciones y traduce direcciones con MMU y TLB.
- **Memoria:** paginación, tablas de páginas y procesos que crecen o se achican.
- **I/O:** dispositivos simulados y un sistema de archivos propio.

**Mi rol:** desarrollé el módulo de **Memoria** y colaboré en la **CPU**.

<details>
<summary>Cómo compilar</summary>

Requiere la [so-commons-library](https://github.com/sisoputnfrba/so-commons-library). Después, en cada módulo (`kernel`, `cpu`, `memoria`, `entradasalida`), ejecutá `make`. El ejecutable queda en `bin/` y se configura con su archivo `.config`.
</details>
