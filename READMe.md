# Taller: Procesamiento de texto

**Curso:** Procesamiento de Lenguaje Natural (PLN)
**Duración:** 2 horas · **Herramienta:** Google Colab · **Textos:** español

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/USUARIO/REPOSITORIO/blob/main/taller_procesamiento_de_texto.ipynb)

> Reemplaza `USUARIO/REPOSITORIO` en el enlace anterior por la ruta real del repositorio una vez subido.

## Objetivo

Recorrer, paso a paso y con código explicado línea por línea, la tubería completa de procesamiento de texto: desde la limpieza básica hasta el uso de modelos de lenguaje preentrenados (Hugging Face) y un LLM abierto. No se requiere experiencia previa en programación.

## Contenido del notebook

| # | Sección | Librería principal |
|---|---|---|
| 0 | Instalación de librerías | — |
| 1 | Corpus de trabajo (8 noticias en español) | `pandas` |
| 2 | Normalización de texto y tokenización | `re`, `nltk` |
| 3 | Stopwords | `nltk` |
| 4 | Stemming | `nltk` (Snowball) |
| 5 | Term Frequency (TF) | `scikit-learn` |
| 6 | Inverse Document Frequency (IDF) y TF-IDF | `scikit-learn` |
| 7 | Lematización | `spaCy` |
| 8 | Part-of-Speech Tagging | `spaCy` |
| 9 | Parsing (dependencias) | `spaCy` |
| 10 | Named-Entity Recognition | `spaCy` |
| 11 | Text mining (nube de palabras, n-gramas, clustering) | `wordcloud`, `scikit-learn` |
| 12 | Sentence Similarity | `sentence-transformers` |
| 13 | Text Classification (clásica, sentimiento, zero-shot) | `scikit-learn`, `transformers` |
| 14 | Question Answering | `transformers` |
| 15 | Summarization | `transformers` |
| 16 | Translation | `transformers` |
| 17 | Text Generation (GPT-2 en español) | `transformers` |
| 18 | Generación de texto usando un LLM (Qwen2.5-0.5B-Instruct) | `transformers` |
| 19 | Cierre, entrega y rúbrica | — |

## Modelos utilizados (todos gratuitos, sin API key)

| Tarea | Modelo | Tamaño aprox. |
|---|---|---|
| Análisis lingüístico | `es_core_news_sm` (spaCy) | 12 MB |
| Similitud de oraciones | `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2` | 120 MB |
| Sentimiento | `finiteautomata/beto-sentiment-analysis` | 440 MB |
| Clasificación zero-shot | `MoritzLaurer/mDeBERTa-v3-base-mnli-xnli` | 560 MB |
| Preguntas y respuestas | `PlanTL-GOB-ES/roberta-base-bne-sqac` | 500 MB |
| Resumen | `mrm8488/bert2bert_shared-spanish-finetuned-summarization` | 500 MB |
| Traducción | `Helsinki-NLP/opus-mt-es-en` y `opus-mt-en-es` | 300 MB c/u |
| Generación de texto | `datificate/gpt2-small-spanish` | 500 MB |
| LLM | `Qwen/Qwen2.5-0.5B-Instruct` | 1 GB |

## Agenda sugerida (2 horas)

| Tiempo | Bloque | Secciones |
|---|---|---|
| 0:00 – 0:10 | Instalación y corpus de trabajo | 0 – 1 |
| 0:10 – 0:40 | Preprocesamiento clásico | 2 – 6 |
| 0:40 – 1:00 | Análisis lingüístico con spaCy | 7 – 9 |
| 1:00 – 1:20 | Representación numérica y minería de texto | 10 – 11 |
| 1:20 – 1:55 | Tareas con modelos preentrenados y LLM | 12 – 18 |
| 1:55 – 2:00 | Cierre y entrega | 19 |

## Recomendaciones para la sesión

- Pedir a los estudiantes que activen la GPU en Colab (`Entorno de ejecución → Cambiar tipo de entorno de ejecución → T4 GPU`) y ejecuten la celda de instalación **antes** de que empiece la clase.
- Las secciones 12 a 18 descargan modelos; si el internet del aula es limitado, conviene ejecutarlas una vez al inicio para que queden en caché.
- Cada sección termina con un ejercicio ✏️ corto; se pueden hacer en clase o dejar para la entrega.

## Entrega

1. Reemplazar el corpus por al menos 8 textos propios en español con mínimo 3 categorías.
2. Ejecutar el notebook completo y resolver los ejercicios ✏️.
3. Agregar una celda final con conclusiones (mínimo 10 líneas).
4. Subir el notebook con resultados al repositorio de GitHub del estudiante y entregar el enlace.

### Rúbrica

| Criterio | Puntos |
|---|---|
| Corpus propio procesado por la tubería clásica (secciones 2–11) | 30 |
| Tareas con modelos preentrenados sobre el corpus propio (12–18) | 30 |
| Ejercicios ✏️ resueltos y comentados | 25 |
| Conclusiones argumentadas | 15 |

## Referencias

- Curso gratuito de Hugging Face: https://huggingface.co/learn/nlp-course
- spaCy en español: https://spacy.io/models/es
- Jurafsky & Martin, *Speech and Language Processing* (gratuito): https://web.stanford.edu/~jurafsky/slp3/
