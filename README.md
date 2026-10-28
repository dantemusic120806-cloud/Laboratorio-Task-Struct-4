# Laboratorio-Task-Struct-4
Para terminar rápido y sin complicaciones, aquí tienes un **resumen directo y listo para copiar y pegar** en tu Word o repositorio de GitHub para esta actividad del Módulo U1-F4:

---

# INFORME DE LABORATORIO: RADIOGRAFÍA DEL KERNEL Y EL SISTEMA DE ARCHIVOS `/proc`

## 1. Introducción y la Naturaleza de `/proc`

* Herramientas de monitoreo como `ps`, `top` o `htop` no utilizan APIs secretas; leen texto plano directamente del sistema de archivos virtual y dinámico `/proc`.


* Los archivos dentro de `/proc` no ocupan espacio en disco (tamaño de 0 bytes) y son generados al vuelo por el kernel a partir de las estructuras internas como el `task_struct`.



## 2. Anatomía de la Memoria y Descriptores (`/status`, `/maps`, `/fd`)

* **VmSize:** Memoria virtual total comprometida o mapeada ("promesa").


* **VmRSS:** Páginas físicas ocupándose en la RAM real en ese instante ("realidad").


* **VmSwap:** Páginas desalojadas al disco duro.


* El directorio `/fd` lista los descriptores de archivos abiertos, sirviendo como base fundamental para herramientas como `lsof`.



## 3. Fotografías Estáticas vs. Vistas Dinámicas

* **Estáticas (Nacimiento):** Archivos como `/cmdline` y `/environ` que se congelan con los argumentos y variables exactas en el momento del `fork/exec` y no vuelven a cambiar.


* **Dinámicas (En Vivo):** Archivos como `/status`, `/stat`, `/maps` y `/fd` que mutan constantemente reflejando el consumo real de CPU y RAM.



## 4. Conclusión

El sistema de archivos `/proc` actúa como el puente esencial entre el espacio de usuario y las estructuras profundas del kernel (`task_struct`), permitiendo auditar y diagnosticar con total precisión el comportamiento en tiempo real de los procesos en Linux.

---

Copia esto directamente, súbelo a tu GitHub o guárdalo en tu Word y habrás terminado la actividad de forma rápida.
