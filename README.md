# 📊 TweetFuzzySentimentAnalysis

Este proyecto implementa un sistema de análisis de sentimiento difuso basado en el artículo de investigación:
> [**Vashishtha, S., & Susan, S. (2019).**](https://www.researchgate.net/profile/Srishti-Vashishtha-2/publication/334622166_Fuzzy_Rule_based_Unsupervised_Sentiment_Analysis_from_Social_Media_Posts/links/5ece42174585152945149e5b/Fuzzy-Rule-based-Unsupervised-Sentiment-Analysis-from-Social-Media-Posts.pdf)_Fuzzy rule based unsupervised sentiment analysis from social media posts._ Expert Systems with Applications, 138, 112834

El objetivo es analizar sentimientos en tweets utilizando un enfoque difuso, que proporciona una clasificación más matizada de los datos que los métodos de análisis de sentimiento tradicionales.


## 📖Tabla de Contenido

 - [Descripcion](#descripcion)
 - [Caracteristicas](#caracteristicas)
 - [Requisitos](#requisitos)
 - [Instalacion](#instalacion)
 - [Uso](#uso)
 - [Estructura del Proyecto](#estructura-del-proyecto)
 - [Ejemplo de Salida](#ejemplo-de-salida)
 - [Licencia](#licencia)


## 📘Descripcion
El proyecto implementa seis módulos fundamentales para realizar un análisis de sentimiento difuso en tweets, siguiendo las metodologías y especificaciones del artículo de referencia. El sistema permite clasificar tweets en categorías de sentimiento (positivo, negativo, neutral) mediante el uso de un enfoque de lógica difusa y utilizando el dataset Sentiment140.

## ⭐Caracteristicas

✔️ **Preprocesamiento del Dataset**: Implementación de métodos de limpieza y transformación de texto para preparar el dataset de acuerdo con la sección 3.1 del artículo. <br> 
✔️ **Análisis Léxico de Sentimientos**: Uso de un lexicón de sentimientos con la biblioteca NLTK para calcular puntajes positivos y negativos de cada tweet. <br>
✔️ **Fuzzificación de Datos**: Aplicación de técnicas de fuzzificación para representar los puntajes de sentimiento en un formato difuso. <br>
✔️ **Base de Reglas Difusas**: Creación de una base de reglas para inferir el sentimiento general de cada tweet usando la biblioteca scikit-fuzzy. <br>
✔️ **Defuzzificación**: Obtención de un puntaje de sentimiento claro mediante defuzzificación. <br>
✔️ **Benchmarks**: Análisis del rendimiento del sistema mediante benchmarks, incluyendo tiempos de ejecución promedio y conteos de tweets clasificados en cada categoría de sentimiento.


## ✅Requisitos   

Este proyecto utiliza Python 3.8 y las siguientes dependencias, especificadas en `requirements.txt`:

```bash
click==8.1.7
colorama==0.4.6
joblib==1.4.2
nltk==3.9.1
numpy==2.1.2
packaging==24.1
pandas==2.2.3
python-dateutil==2.9.0.post0
pytz==2024.2
regex==2024.9.11
scikit-fuzzy==0.5.0
scipy==1.14.1
six==1.16.0
tqdm==4.66.6
tzdata==2024.2
```


## ⚙Instalacion
Para instalar y configurar el proyecto en tu máquina local, sigue estos pasos:

1. Clona el repositorio:
```bash
   git clone https://github.com/ShoniG19/TweetFuzzySentimentAnalysis.git
```

2. Navega al directorio del proyecto:
```bash
   cd TweetFuzzySentimentAnalysis
```  

3. Instala las dependencias:
```bash
   pip install -r requirements.txt
``` 
## 🚀Uso
Para ejecutar el análisis de sentimiento en los tweets:
1. Ejecuta el script principal main.py:
```bash
   python main.py
```


## 🗂Estructura del Proyecto

```bash
📁 TweetFuzzySentimentAnalysis/
├── 📁 data/               # Archivos de datos de entrada
│   ├── train_data.csv     # Dataset de entrenamiento
│   └── test_data.csv      # Dataset de prueba
├── 📁 output/             # Resultados del análisis
│   └── output.csv         # Archivo de salida
├── main.py                # Script principal del proyecto
├── requirements.txt       # Dependencias del proyecto
└── README.md              # Documentación del proyecto
```
#### Descripción de Archivos
- `data/test_data.csv`: Archivo dataset de prueba extraido de [Kaggle.com](https://www.kaggle.com/datasets/krishbaisoya/tweets-sentiment-analysis) 
- `output/output.csv`: Archivo de resultados que incluye los puntajes de sentimiento y otros datos para cada tweet.
- `main.py`: Script principal que ejecuta el flujo de análisis completo desde la carga de datos hasta la exportación de resultados.


## 🔍Ejemplo de Salida
El archivo de salida `output/output.csv` contiene las siguientes columnas:

- `Oración Original`: Texto del tweet original.
- `Label Original`: Etiqueta de sentimiento inicial.
- `Puntaje Positivo`: Puntaje de sentimiento positivo calculado.
- `Puntaje Negativo`: Puntaje de sentimiento negativo calculado.
- `Puntaje Neutro`: Puntaje de sentimiento neutro calculado.
- `Clasificacion`: Clasificacion del tweet
- `Tiempo de Ejecución`: Tiempo que tomó procesar cada tweet individualmente.
- `Tiempo de Fuzzificacion`: Tiempo que tomó fuzzificar cada tweet individualmente.
- `Tiempo de Defuzzificacion`: Tiempo que tomó defuzzificar cada tweet individualmente.

![image](https://github.com/user-attachments/assets/533d2325-ffa5-465a-8c46-e9e1dec59313)


## 📜Licencia

Este proyecto está licenciado bajo la licencia [MIT](LICENSE).

