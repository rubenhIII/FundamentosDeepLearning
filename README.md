# Fundamentos de Deep Learning con PyTorch

**Curso introductorio para estudiantes de TIC y Seguridad**  
**Instructor:** Dr. Rubén Hernández Torres  
**Duración estimada:** 3 sesiones de 2 horas (6 horas en total)

## Descripción

Este repositorio reúne las presentaciones, notebooks, ejemplos y recursos de un curso introductorio de **Deep Learning con PyTorch**, orientado a estudiantes con conocimientos de programación en Python e interés en redes, sistemas y ciberseguridad.

El curso busca comprender **cómo funcionan y se entrenan diferentes arquitecturas neuronales**, no solamente ejecutar modelos preconstruidos. Los ejercicios conectan los fundamentos matemáticos y de programación con problemas de regresión, clasificación de texto, procesamiento de secuencias y uso de modelos preentrenados.

> **Repositorio en desarrollo:** el contenido, los notebooks y la organización pueden cambiar durante el curso. Algunos ejercicios y archivos descritos aquí son actividades previstas y se incorporarán progresivamente.

## Objetivos de aprendizaje

Al finalizar, se espera que los participantes puedan:

- Explicar el funcionamiento básico de una red neuronal y su proceso de entrenamiento.
- Utilizar tensores, diferenciación automática y módulos de PyTorch.
- Distinguir problemas de regresión y clasificación, así como sus funciones de pérdida y métricas.
- Representar texto mediante tokens y embeddings.
- Comprender por qué el orden de una secuencia importa y cómo se modela mediante RNN y GRU.
- Identificar los principios de *self-attention* y de la arquitectura Transformer.
- Realizar inferencia con modelos preentrenados y reconocer consideraciones básicas para integrar un modelo en una aplicación.

## Contenido por día

### Día 1 — Redes neuronales y entrenamiento

**Fundamentos de Deep Learning con PyTorch**

- Deep Learning y aplicaciones en redes, sistemas y seguridad.
- Neurona artificial, capas densas y redes *feed-forward* (MLP).
- Funciones de activación, pérdida, gradiente y retropropagación.
- Entrenamiento y optimización de parámetros.
- Tensores, `autograd`, `Dataset` y `DataLoader`.
- Diferencias entre clasificación y regresión.

**Práctica orientativa:** construir y entrenar una MLP para un problema de regresión, por ejemplo, predicción de rendimiento relativo de hardware.

**Material:** [Presentación del día 1](documentacion/dia01.pdf)

### Día 2 — Embeddings, RNN y GRU

**Deep Learning para texto y secuencias**

- Tokenización, vocabulario y representación *one-hot*.
- Embeddings aprendibles con `nn.Embedding`.
- Secuencias de longitud variable, padding y máscaras.
- Clasificación de texto mediante embeddings y agregación (*pooling*).
- Redes recurrentes, estado oculto y retropropagación a través del tiempo.
- Conceptos de LSTM y GRU.
- Clasificación de secuencias y evaluación mediante precision, recall y F1-score.

**Práctica orientativa:** clasificar mensajes legítimos y sospechosos y comparar un modelo con *mean pooling* frente a otro con GRU, observando el efecto del orden de los tokens.

**Material:** [Presentación del día 2](documentacion/dia02.pdf)

### Día 3 — Transformers y aplicaciones

**Atención, modelos preentrenados y despliegue**

- Limitaciones de las redes recurrentes.
- *Self-attention*, Query, Key y Value.
- *Scaled dot-product attention* y atención multicabeza.
- Información posicional y componentes de un Transformer.
- Preentrenamiento, aprendizaje por transferencia e inferencia.
- Uso introductorio de modelos disponibles en Hugging Face.
- Guardado y carga de modelos con PyTorch.
- Integración básica de inferencia en aplicaciones; ejemplo con Gradio.
- Consideraciones de seguridad, evaluación y uso responsable.

**Práctica orientativa:** explorar un Transformer pequeño para clasificación y ejecutar inferencia con un modelo preentrenado. Como cierre, plantear una aplicación de Deep Learning para redes, sistemas o seguridad.

**Material:** [Presentación del día 3](documentacion/dia03.pdf)

## Organización del repositorio

```text
.
├── README.md
├── dia01/
│   ├── README.md                 # Opcional: guía de la sesión
│   └── notebooks/                # Prácticas del día 1
├── dia02/
│   ├── README.md                 # Opcional: guía de la sesión
│   └── notebooks/                # Prácticas del día 2
├── dia03/
│   ├── README.md                 # Opcional: guía de la sesión
│   └── notebooks/                # Prácticas del día 3
└── documentacion/
    ├── dia01.pdf
    ├── dia02.pdf
    └── dia03.pdf
```

La estructura es una propuesta inicial. Los archivos de práctica y las guías específicas se añadirán conforme avance el curso. Los enlaces a las presentaciones funcionarán cuando los PDF se ubiquen en `documentacion/`.

## Requisitos previos

- Conocimientos básicos de **Python**: funciones, estructuras de datos y clases.
- Familiaridad con programación orientada a objetos.
- Conocimientos básicos de álgebra y operaciones con vectores y matrices son recomendables, pero se revisarán los conceptos esenciales.
- Uso básico de notebooks Jupyter o Google Colab.

**No se requiere experiencia previa en Deep Learning.**

## Preparación del entorno

Se recomienda utilizar **Google Colab** o un entorno local con Python y Jupyter.

Para un entorno local:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install torch numpy pandas matplotlib scikit-learn jupyter
```

Las prácticas que utilicen Hugging Face, Gradio o datasets de UCI pueden requerir paquetes adicionales:

```bash
python -m pip install transformers gradio ucimlrepo
```

> La instalación de PyTorch con soporte GPU depende del sistema operativo y de la plataforma de cómputo. Consulta las instrucciones oficiales para seleccionar la versión adecuada.

## Metodología

Cada sesión combina una introducción conceptual, revisión de componentes de PyTorch y experimentos guiados. Se promoverá la modificación de arquitecturas, la comparación de resultados y la discusión de sus limitaciones.

Los datasets pequeños y los ejemplos sintéticos se utilizan con **fines educativos**. Obtener buena exactitud sobre datos de juguete no demuestra que un modelo sea adecuado para un entorno real, especialmente en aplicaciones de seguridad.

## Referencias y recursos

- [Documentación oficial de PyTorch](https://docs.pytorch.org/docs/stable/index.html)
- [Tutoriales de PyTorch](https://docs.pytorch.org/tutorials/)
- [Hugging Face Transformers](https://huggingface.co/docs/transformers/)
- [UCI Machine Learning Repository](https://archive.ics.uci.edu/)
- [Computer Hardware Dataset (UCI)](https://archive.ics.uci.edu/dataset/29/computer+hardware)
- [Gradio](https://www.gradio.app/docs)

Las presentaciones del curso se almacenarán en [`documentacion/`](documentacion/). Esta carpeta también podrá incluir lecturas y referencias complementarias.

## Estado del material

El repositorio se actualizará durante el desarrollo del curso. Las actividades prácticas, datasets, dependencias y estructura pueden ajustarse de acuerdo con el avance del grupo.

## Autor

**Dr. Rubén Hernández Torres**  
Material académico para el curso *Fundamentos de Deep Learning con PyTorch*.

