# Ampliación de Contenidos Audiovisuales

Estudiante: Jordy Joel Chambi Romero

Proyecto Java educativo de Programación Orientada a Objetos basado en el ejemplo público de la Unidad 2 de la UPS. Mantiene los paquetes originales `uni1a` y `poo`.

## Objetivo

Modelar contenidos audiovisuales y sus relaciones usando herencia, asociación, agregación y composición.

## Clases y relaciones

- `ContenidoAudiovisual` es la clase abstracta base; `Pelicula`, `SerieDeTV`, `Documental`, `VideoYouTube` y `Cortometraje` la extienden.
- `Pelicula` agrega actores (`Actor`), que pueden existir y reutilizarse independientemente.
- `SerieDeTV` compone temporadas (`Temporada`), cuya vida se administra desde la serie.
- `Documental` se asocia con un investigador (`Investigador`) independiente.
- `VideoYouTube` se asocia con un canal; `Cortometraje` añade datos de producción.

## Requisitos

- JDK 8 o posterior.
- No se requieren dependencias externas.

## Abrir en Eclipse

1. Descomprime el ZIP en una carpeta fácil de encontrar.
2. En Eclipse elige **File > Import... > General > Existing Projects into Workspace**.
3. En **Select root directory**, selecciona la carpeta `ampliacion-contenidos-audiovisuales` que acabas de descomprimir.
4. Marca el proyecto encontrado y pulsa **Finish**. Si Eclipse solicita un JDK, elige Java 8 o posterior en **Window > Preferences > Java > Installed JREs**.
5. Abre `src/main/java/poo/PruebaAudioVisual.java`, haz clic derecho y selecciona **Run As > Java Application**.

La carpeta `evidencias/` enumera capturas sugeridas para documentar la tarea.

## Clonar y ejecutar

```bash
git clone https://github.com/Jordy/ampliacion-contenidos-audiovisuales.git
cd ampliacion-contenidos-audiovisuales
```

En Windows (PowerShell), desde la carpeta del proyecto:

```powershell
New-Item -ItemType Directory -Force out
javac -encoding UTF-8 -d out src/main/java/uni1a/*.java src/main/java/poo/*.java
java -cp out poo.PruebaAudioVisual
```

En macOS/Linux:

```bash
mkdir -p out
javac -encoding UTF-8 -d out src/main/java/uni1a/*.java src/main/java/poo/*.java
java -cp out poo.PruebaAudioVisual
```

La ejecución crea objetos de todas las clases, muestra sus detalles y demuestra cómo agregar/quitar actores y temporadas, así como cambiar el investigador de un documental. `diagrama-clases.svg` es el diagrama visual; `diagrama-clases.puml` contiene su fuente PlantUML.

## Estructura

```text
src/main/java/uni1a/  Clases del dominio
src/main/java/poo/    Programa demostrativo ejecutable
diagrama-clases.puml  Diagrama UML
```

## GitHub

Después de crear el repositorio personal, sustituye `USUARIO` por tu nombre de usuario y agrega el remoto. La creación del repositorio, el push y los commits se realizan desde la cuenta del estudiante.
