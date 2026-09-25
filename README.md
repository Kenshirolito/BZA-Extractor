# BZA-Extractor

BZA-Extractor es una herramienta creada por **Brazil Alliance** para preparar traducciones de juegos de *Yakuza*. Se comparte para que comunidades de otros idiomas puedan crear sus propias traducciones, después de que la herramienta no estuviera disponible públicamente durante estos tres años.

## Juegos compatibles

> [!IMPORTANT]
> **BZA-Extractor solo está habilitada para estos tres juegos:**
>
> - **Yakuza 3 (Legacy)**
> - **Yakuza 4**
> - **Yakuza 5**
>
> Cada juego tiene su propio archivo `.bat`. Usa únicamente el `.bat` correspondiente al juego que quieras traducir.

## Requisitos

- Una instalación de uno de los tres juegos compatibles.
- **ParTool versión 1.3.3**.
- BZA-Extractor.

ParTool es una herramienta externa y no es propiedad de Brazil Alliance. Descárgala desde el repositorio de **Kaplas**. Debe ser exactamente la versión **1.3.3**; otras versiones no son compatibles con esta configuración de BZA-Extractor.

## 1. Configura ParTool

1. Descarga ParTool **1.3.3** desde el repositorio de Kaplas y extrae sus archivos.
2. Abre `bza_config.ini`, incluido con BZA-Extractor.
3. Busca esta línea:

   ```ini
   partool_root=C:\ParTool.exe
   ```

4. Cambia el valor para que apunte a la ubicación real de `ParTool.exe`.

Por ejemplo, si `ParTool.exe` está en `D:\Herramientas\ParTool\ParTool.exe`, deja la línea así:

```ini
partool_root=D:\Herramientas\ParTool\ParTool.exe
```

La ruta predeterminada sirve si colocaste `ParTool.exe` directamente en `C:\`. Si está en otra ubicación, actualiza la ruta del archivo `.ini` antes de continuar.

## 2. Comprueba la ruta del juego

Cada archivo `.bat` está preparado para un juego específico y usa las rutas de instalación predeterminadas de Steam. Si instalaste el juego en otra ubicación, abre el `.bat` correspondiente y ajusta allí la ruta para que coincida con la carpeta donde está instalado ese juego.

## 3. Genera el proyecto de traducción

1. Ejecuta el `.bat` correspondiente al juego que vas a traducir.
2. BZA-Extractor generará por defecto una carpeta `C:\Project`.
3. Dentro de `C:\Project` encontrarás una carpeta con el nombre del juego seleccionado.
4. En esa carpeta del juego encontrarás `workspace`, donde se guardan los archivos `.po` que contienen los textos para traducir.

Si quieres que el proyecto se genere en otra ubicación, edita el `.bat` del juego antes de ejecutarlo y cambia la ruta de salida configurada allí.

## 4. Traduce los archivos `.po`

Abre y traduce los archivos `.po` que están dentro de `workspace`. Conserva la estructura de esos archivos y modifica el texto traducible.

## 5. Compila la traducción

Cuando termines de traducir, ejecuta `compile.bat`, que se encuentra dentro de la carpeta del juego generada en `C:\Project`. Este archivo convierte los `.po` traducidos en la traducción compilada.

## Resumen rápido

1. Descarga **ParTool 1.3.3** desde el repositorio de Kaplas.
2. Configura `partool_root` en `bza_config.ini` para que apunte a `ParTool.exe`.
3. Si hace falta, corrige la ruta del juego en su archivo `.bat`.
4. Ejecuta el `.bat` del juego compatible que quieras traducir.
5. Traduce los `.po` de `workspace`.
6. Ejecuta `compile.bat` para compilar la traducción.
