# Biojuego

**Biojuego** es un juego desarrollado en **JavaScript** y ejecutado directamente en el navegador.

## Estructura del proyecto

```text
.
├── .gitignore
├── appmanifest.json
├── c2runtime.js
├── data.js
├── index.html
├── jquery-2.1.1.min.js
├── offline.js
├── offlineClient.js
├── README.md
├── sw.js
├── images/
└── media/
```

## Archivos principales

- **index.html**: archivo principal que carga el juego.
- **c2runtime.js**: contiene la lógica principal del juego.
- **data.js**: almacena datos utilizados por el juego.
- **jquery-2.1.1.min.js**: biblioteca jQuery usada por el proyecto.
- **offline.js**: maneja funciones relacionadas con el modo offline.
- **offlineClient.js**: cliente de soporte offline.
- **sw.js**: service worker para caché y funcionamiento sin conexión.
- **appmanifest.json**: configuración de la aplicación web.

## Requisitos

Para ejecutar este proyecto necesitas:

- **Python 3** instalado
- Un navegador moderno como **Google Chrome**, **Microsoft Edge** o **Mozilla Firefox**

## Instalación

Este proyecto **no usa `npm install`** porque no incluye archivo `package.json`.

Si ejecutas `npm install`, aparecerá un error `ENOENT` indicando que no se encuentra `package.json`. Esto fue verificado en la ejecución del proyecto. fileciteturn0file0L2-L10

## Ejecución

### Opción recomendada: servidor local

Desde PowerShell, entra a la carpeta del proyecto y ejecuta:

```powershell
cd /d %USERPROFILE%\Desktop\biojuego
python -m http.server 8000
```

Luego abre en tu navegador:

```text
http://localhost:8000
```

El registro de ejecución muestra que el servidor local cargó correctamente `index.html`, scripts, imágenes, audio y `sw.js`. fileciteturn0file0L22-L24 fileciteturn0file0L25-L29 fileciteturn0file0L179-L180

### Opción alternativa: abrir el archivo directamente

En PowerShell, escribir solo:

```powershell
index.html
```

no funciona como comando directo. PowerShell indica que, si quieres abrir el archivo desde la carpeta actual, debes usar:

```powershell
.\index.html
```


> Nota: aunque `./index.html` puede abrir el archivo, la opción recomendada sigue siendo `python -m http.server 8000`, especialmente si el juego usa `sw.js`, caché o modo offline.

## Contribución

Si deseas contribuir al proyecto, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama:
   ```bash
   git checkout -b feature/nueva-funcionalidad
   ```
3. Realiza tus cambios y guarda el progreso:
   ```bash
   git add .
   git commit -m "Añadir nueva funcionalidad"
   ```
4. Sube tu rama al repositorio remoto:
   ```bash
   git push origin feature/nueva-funcionalidad
   ```
5. Abre un Pull Request.

## Licencia

Este proyecto está licenciado bajo la **Licencia MIT**.
Consulta el archivo `LICENSE` para más detalles.
