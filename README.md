# Espacios de color aplicados a visión por ordenador

Cuaderno Jupyter para explorar y comparar distintos espacios de color utilizados en visión por ordenador mediante OpenCV y Matplotlib.

## Contenido

Se trabajan los siguientes espacios de color:

- RGB
- HSV
- CIELAB (Lab)
- YCrCb
- Escala de grises e imagen binaria
- XYZ

El cuaderno incluye la carga de imágenes, las conversiones entre espacios de color, la visualización de sus canales y una explicación breve de sus principales aplicaciones.

## Estructura

```text
espacios-color-cv/
├── README.md
├── espacios_color.ipynb
├── requirements.txt
└── data/
    ├── colores.png
    ├── objeto_color.png
    ├── iluminacion.png
    ├── persona.png
    └── qr.png
```

## Imágenes seleccionadas

- `colores.png`: imagen con frutas y colores intensos para RGB y XYZ.
- `objeto_color.png`: balón sobre césped, adecuada para explicar HSV y la separación por tono/color.
- `iluminacion.png`: escena urbana nocturna con luces y sombras, adecuada para Lab.
- `persona.png`: retrato, empleado para YCrCb por su uso habitual en vídeo y análisis de crominancia.
- `qr.png`: código QR, empleado para escala de grises y binarización.

## Requisitos

- Python 3.11 o superior recomendado.
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

Las versiones utilizadas para preparar esta entrega están indicadas en `requirements.txt`.

## Instalación y ejecución

### 1. Crear un entorno virtual

En Windows:

```bash
python -m venv .venv
.venv\\Scripts\\activate
```

En Linux/macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2. Instalar las dependencias

```bash
pip install -r requirements.txt
```

### 3. Abrir Jupyter

```bash
jupyter notebook
```

Abrir el archivo `espacios_color.ipynb` y ejecutar las celdas en orden mediante **Run All**.

## Nota sobre OpenCV

OpenCV carga las imágenes en orden **BGR**, mientras que Matplotlib espera **RGB**. Por ello, antes de visualizar una imagen cargada con `cv2.imread()`, se realiza la conversión `cv2.COLOR_BGR2RGB`.

## Objetivo académico

El objetivo es comprender qué información separa cada espacio de color y por qué determinados espacios resultan más adecuados que otros según la tarea de visión por ordenador.
