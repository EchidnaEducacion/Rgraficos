# Recursos gráficos de Echidna

Repositorio central de los recursos gráficos del proyecto **Echidna**: logos, fotografías de las
placas, esquemas, capturas de EchidnaML (EchidnaBlocks y LearningML), portadas de proyectos y
material de difusión.

Hasta ahora las imágenes estaban repartidas y duplicadas entre varios repositorios:

- [manual](https://github.com/EchidnaEducacion/manual) — Manual de EchidnaBlack2 y EchidnaML
- [GuiaInicioEchidnaML](https://github.com/EchidnaEducacion/GuiaInicioEchidnaML) — Guía de inicio de EchidnaML
- [EchidnaEducacion.github.io](https://github.com/EchidnaEducacion/EchidnaEducacion.github.io) — Web

El objetivo de este repositorio es **centralizarlas en una única fuente** y **aumentar su calidad**
(mayor resolución, formatos adecuados y archivos editables originales).

## Estructura

```
logos/
  echidna/              Logo de Echidna (svg, png) y fuentes editables
  echidnaml/            Logo e iconos de EchidnaML
hardware/
  echidnablack2/        Fotos, lupas y esquemas de la placa y sus componentes
  complementos/         Servomotores, sensor de infrarrojos, sensor de humedad...
  placas-anteriores/    EchidnaBlack y EchidnaShield
software/
  echidnaml/            Diagramas y capturas generales (puesta en marcha, descarga, conexión)
  echidnablocks/        Capturas del entorno, bloques y programas de ejemplo
  learningml/           Capturas de las fases, entrenamiento y prueba de modelos
  arduino-ide/          Capturas del IDE de Arduino
proyectos/              Portadas y animaciones de proyectos y actividades
difusion/               Trípticos, carteles, imágenes para redes sociales, pegatinas
plantillas/             Plantillas de portadas y diapositivas
```

Cada carpeta puede tener una subcarpeta `fuentes/` con los archivos editables
(`.ai`, `.svg` maestro, `.xcf`, `.kra`, `.fzz` de Fritzing...) a partir de los cuales se exportan
las imágenes de esa carpeta.

## Convención de nombres

- Todo en **minúsculas** y en **kebab-case** (palabras separadas por guiones).
- **Sin tildes, eñes ni espacios**: `senal-sin-puente.png`, no `Señal sin puente.png`.
- En español.
- Patrón: `<tipo>-<sujeto>[-<variante>].<ext>`

| Prefijo | Uso | Ejemplo |
|---|---|---|
| `logo-` | Logotipos | `logo-echidna-izquierda.png` |
| `icono-` | Iconos | `icono-echidnablocks.png` |
| `foto-` | Fotografías | `foto-echidnablack2-cenital.jpg` |
| `lupa-` | Detalle ampliado de una zona de la placa | `lupa-leds.png` |
| `esquema-` | Esquemas eléctricos | `esquema-led-rgb.png` |
| `conexion-` | Cómo conectar un complemento | `conexion-servomotor.png` |
| `bloque-` | Un bloque de EchidnaBlocks | `bloque-led-verde.png` |
| `programa-` | Programa de ejemplo completo | `programa-semaforo.png` |
| `captura-` | Capturas de pantalla de software | `captura-entorno-learningml.png` |
| `diagrama-` | Diagramas explicativos | `diagrama-puesta-en-marcha.png` |
| `portada-` | Portadas de proyectos, diapositivas o entradas | `portada-hola-mundo.png` |
| `animacion-` | GIF animados | `animacion-semaforo.gif` |
| `triptico-`, `cartel-` | Material de difusión | `triptico-echidna.pdf` |

**Variantes** al final del nombre, solo cuando hagan falta:

- Color: `-negativo`, `-blanco`, `-naranja`
- Orientación: `-izquierda`, `-derecha`, `-horizontal`, `-vertical`
- Idioma: `-gl`, `-en` (sin sufijo = español)
- Placa: `-black2`, `-shield`, si el mismo sujeto existe en varias placas

**No** incluir fechas, `final`, `v2`, `nuevo`... en el nombre: el historial lo lleva git.

Ejemplos de renombrado:

| Antes | Después |
|---|---|
| `Lupa_Ledes.png` | `lupa-leds.png` |
| `Bloque_LEDRGB_NaranajaEchidna.png` | `bloque-led-rgb-naranja.png` |
| `Ejempo_temperatura.png` | `programa-temperatura.png` |
| `Entorno_LearningML.png` | `captura-entorno-learningml.png` |
| `Logo_Echidna_Final.svg` | `logo-echidna.svg` |

## Criterios de calidad

- **Formatos**
  - SVG para logos, iconos y diagramas vectoriales.
  - PNG para capturas de pantalla, bloques y esquemas (fondo transparente cuando tenga sentido).
  - JPG para fotografías.
  - GIF solo para animaciones cortas.
- **Resolución**: las fotos con lado largo de al menos 2000 px; las capturas, a ser posible,
  a doble densidad (2x).
- **Originales**: guardar siempre aquí la versión de mayor calidad. La optimización para web
  (redimensionar, convertir a WebP...) se hace en el repositorio que la usa.
- **Fuentes editables**: si la imagen se ha creado con un programa de diseño, subir el archivo
  original a la carpeta `fuentes/` correspondiente.
- **Fotos de móvil**: eliminar los metadatos EXIF (ubicación, modelo del teléfono) antes de subirlas,
  por ejemplo con `exiftool -all= foto.jpg`.

## Cómo usar estas imágenes en otros repositorios

Copia la imagen desde este repositorio al repositorio que la necesita, manteniendo el mismo nombre,
y optimízala allí para su uso. Si se mejora una imagen, se actualiza primero aquí y después se copia
de nuevo a los repositorios que la usan.

## Cómo contribuir

1. Coloca la imagen en la carpeta temática que corresponda.
2. Nómbrala siguiendo la convención anterior.
3. Si existe, añade el archivo editable en `fuentes/`.
4. Antes de añadir una imagen, comprueba que no exista ya con otro nombre.

## Licencia

Los recursos de este repositorio se distribuyen bajo la licencia
[Creative Commons Atribución-CompartirIgual 4.0 (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.es).
