# Tesis 

*"Técnicas y metodologías para la implementación de sistemas de visión en All Programmable SoCs utilizando síntesis de alto nivel"*

Este repositorio contiene el documento completo de mi tesis de grado para el título de Licenciado en Ciencias de la Computación (FCEN, UBA)  y las diapositivas usadas en la defensa de la misma.

## Objetivo de la tesis
La tesis consistió en analizar la construcción de soluciones de visión artificial sobre AP SoCs, considerando:
- Metodología para el ciclo completo de desarrollo.
- Aceleración por hardware utilizando Síntesis de Alto Nivel
(HLS).
- Diseño de todas las capas del sistema.
- Potencia de Processing System (PS) vs Processing System + Lógica Programable (PL).
- Herramientas disponibles


## Desarrollo
El desarrollo se realizó sobre un chip AP SoC Zynq-7010, el mismo incluye, entre otros componentes:
- ARM Cortex-A9 Dual Core a 650Mhz
- Lóica programable (FPGA)

Como caso de estudio, partiendo de LIBVISO2, implementé una solución de Odometría Visual Estéreo delegando parte del trabajo a IP Cores implementados en lógica programable utilizando síntesis de alto nivel.

El software de la solución utiliza Linux como sistema operativo y se comunica con la lógica programable mediante un módulo del kernel que implementé. El módulo hace uso de mmap, IOCTL y la API dma de Linux.