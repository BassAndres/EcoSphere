# Abrir EcoSphere en Visual Studio

Igual que en las prácticas: no hace falta CMake ni instalar GLFW.

1. Abre `EcoSphere.sln` con doble clic.
2. Arriba elige **Debug** y **x64**.
3. Presiona **Depurador local de Windows** (o F5). La primera vez compila todo y tarda un par de minutos.

La solución tiene dos proyectos:

| Proyecto | Código | Shaders |
| --- | --- | --- |
| `EcoSphere` | `src/` (el original) | `assets/common/shaders/` |
| `EcoSphereLegible` | `legible/src/` | `legible/shaders/` |

El que está en negritas en el Explorador de soluciones es el que corre. Para cambiarlo: clic derecho,
**Establecer como proyecto de inicio**.

## Qué hace al compilar

- Usa GLFW 3.4 de `deps/glfw/MSVC2022`, la misma versión de la plantilla del laboratorio.
- Deja el ejecutable en `bin/<proyecto>/<Debug|Release>/ecosphere.exe`.
- Copia junto al ejecutable los shaders y los modelos (`shaders/` y `assets/`). Si cambias un shader o
  un `.glb`, vuelve a compilar para que se copie.

## Argumentos

Ya viene con `--plaza` en **Propiedades → Depuración → Argumentos de comandos**. Otras opciones:

- `--module aquabio --content` (o `ecoenergy`, `ecocycle`): entra directo a una zona.
- Si pones un argumento que no existe, la consola muestra la lista completa de opciones.

Las carpetas `bin/`, `obj/` y `.vs/` se generan solas y no se suben al repositorio.
