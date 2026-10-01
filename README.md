# Scratch en movimiento

Guía interactiva en español creada por Yunga para aprender programación con Scratch, desde el uso de bloques hasta juegos con cámara. Proyecto independiente, sin afiliación oficial a Scratch.

## Incluye

- 8 lecciones con pasos, secuencias y un reto final: escenario, secuencias, bucles, puntuación, cámara y 3 juegos.
- 11 categorías para explorar bloques, incluidas Detección de video y Detección de rostro.
- Taller de secuencias con movimiento, giro, espera, orden de ejecución y repetición.
- Laboratorio de objetivos de 30 segundos: modo táctil/puntero y detección local de movimiento con webcam.
- Diseño adaptable a móvil y computadora, navegación por teclado, progreso local y caché sin conexión después de una primera visita en línea.

## Publicar en GitHub Pages

1. En este repositorio, abre **Settings → Pages**.
2. En **Build and deployment**, selecciona **Deploy from a branch**.
3. Elige **main** y **/(root)**. Pulsa **Save**.
4. Espera el despliegue. La dirección prevista es https://yunga18.github.io/Scratch-IA/ .

El editor externo de Scratch y los recursos oficiales requieren conexión. La cámara de esta guía requiere HTTPS o localhost. Los navegadores compatibles pueden ofrecer añadir o instalar la guía en la pantalla de inicio; no se incluye un APK.

## Ejecutar localmente

```sh
python -m http.server 8000
```

Abre http://localhost:8000 . No hace falta instalar dependencias ni crear una base de datos. Abrir el HTML como archivo no activa las capacidades de cámara y caché de manera fiable.

## Cámara y datos

La cámara se solicita únicamente al iniciar una partida con el control Cámara seleccionado. Se procesa en memoria, sin grabaciones ni envíos. Al detener, navegar fuera del laboratorio o esconder la página se cierran las pistas de video. La demostración compara cambios de píxeles dentro del objetivo, sin reconocimiento facial ni seguimiento del esqueleto. Los tutoriales de rostro se construyen en el editor real de Scratch.

El progreso se guarda con localStorage en el navegador actual. No se sincroniza entre dispositivos. Si se borra el almacenamiento del sitio, se elimina. Si el navegador bloquea el almacenamiento, funciona temporalmente durante la sesión.

## Editar

- `content.js`: categorías, lecciones, secuencias y preguntas.
- `app.js`: navegación, progreso, taller y laboratorio.
- `styles.css`: diseño adaptable.
- `sw.js`: caché local; incrementa el nombre de caché cuando cambies la lista de archivos.
- `manifest.webmanifest` e `icon.svg`: datos de instalación y marca.

Las secuencias mostradas son instrucciones para reconstruir en Scratch, no proyectos `.sb3`. El taller es una simulación limitada, no ejecuta programas generales de Scratch. Los umbrales de la demostración no son equivalentes a los valores de Video Sensing.

## Fuentes oficiales consultadas

- [Editor de Scratch](https://scratch.mit.edu/projects/editor/)
- [Detección de video](https://scratchfoundation.org/learn/learning-library/video-sensing)
- [Detección de rostro](https://scratchfoundation.org/learn/learning-library/face-sensing)
- [Face Sensing: posibilidades y privacidad](https://scratchfoundation.org/tools/scratch-lab/face-sensing)
- [Biblioteca de aprendizaje](https://scratchfoundation.org/learn/learning-library)

Ejercicios y explicaciones redactados para esta guía. Las traducciones de etiquetas pueden cambiar según la versión e idioma del editor.
