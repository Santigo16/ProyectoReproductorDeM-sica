# Reproductor de Música en Python

Este proyecto es un reproductor de música desarrollado en Python
utilizando **Pygame**, **Flet** y **Mutagen**. Permite cargar canciones,
reproducirlas, pausar, detener, visualizar su duración y gestionar una
lista básica de archivos MP3.

## Características principales

-   Reproducción de archivos MP3.
-   Obtención automática del título y duración de cada canción.
-   Interfaz gráfica construida con **Flet**.
-   Control de reproducción: reproducir, pausar, continuar y detener.
-   Lectura de metadatos mediante **Mutagen**.
-   Manejo de rutas y archivos con la librería **os**.

## Tecnologías utilizadas

### **Python 3**

Lenguaje principal para la lógica del reproductor.

### **Pygame**

Usado para: - Inicializar el módulo de audio. - Reproducir, pausar y
detener archivos MP3.

### **Flet**

Usado para: - Crear la interfaz gráfica multiplataforma. - Manejar
eventos y actualizaciones en la UI.

### **Mutagen**

Usado para: - Leer metadatos de los archivos MP3. - Obtener la duración
real de las canciones.

### **os**

Usado para: - Acceder a archivos y directorios. - Extraer nombres de
archivo con `os.path`.

### **asyncio**

Usado para: - Manejar funciones asíncronas dentro de Flet. - Permitir
que la UI siga funcionando mientras se reproduce música.

------------------------------------------------------------------------

# Estructura del proyecto

    ProyectoReproductorDeMusica/
    │
    ├── main.py                # Lógica principal del reproductor y la interfaz
    ├── Song.py                # Clase Song que representa cada canción
    ├── assets/                # Carpeta para almacenar archivos de música
    └── README.md

## Clase `Song`

La clase `Song` representa una canción individual.\
Características:

-   Almacena el nombre del archivo.
-   Extrae un título a partir del nombre.
-   Obtiene la duración real con `Mutagen`.

Ejemplo de uso:

``` python
cancion = Song("mi_tema.mp3")
print(cancion.title)
print(cancion.duration)
```

------------------------------------------------------------------------

# Cómo ejecutar el proyecto

## 1. Instalar dependencias

``` bash
pip install pygame flet mutagen
```

## 2. Agregar archivos MP3

Coloca tus canciones dentro de la carpeta `assets/`.

## 3. Ejecutar el programa

``` bash
python main.py
```

------------------------------------------------------------------------

# Funcionalidades implementadas

-   Carga dinámica de canciones desde un directorio.
-   Reproducción secuencial.
-   Visualización del título de la canción en pantalla.
-   Actualización del estado del reproductor mediante Flet.
-   Control del flujo de audio con Pygame.
-   Obtención de duración real del audio con Mutagen.

------------------------------------------------------------------------

# Posibles mejoras futuras

-   Barra de progreso para cada canción.
-   Soporte para listas de reproducción.
-   Botones de siguiente y anterior.
-   Visualizador gráfico de audio.
-   Más información de metadatos (artista, álbum, etc.).
