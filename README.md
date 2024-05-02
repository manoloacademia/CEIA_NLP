# Repositorio de la materia Procesamiento del Lenguaje Natural (CEIA-FIUBA).
## Autor: Pablo Segovia
- Cohorte: 12.
- Año: 2024

# Resumen
El presente repositorio describe los desafíos realizados en la materia Procesamiento del Lenguaje Natural de la Especialización en Inteligencia Artificial de la FIUBA.
Los desafíos realizados son:

## Desafío 1 
El [Desafío 1](https://github.com/manoloacademia/CEIA_NLP/blob/main/Desafio_1_PabloSegovia.ipynb) soluciona un problema de similitud realizando una vectorización de texto y modelo de clasificación Naïve Bayes con el dataset [20 newsgroups](https://scikit-learn.org/0.19/datasets/twenty_newsgroups.html).
Para poder resolverlo

## Desafío 2
- El [Desafío 2](https://github.com/manoloacademia/CEIA_NLP/blob/main/Desafio_2_PabloSegovia.ipynb) es utilizar documentos / corpus para crear embeddings de palabras basado en ese contexto.
- Se utilizó el libro [Crimen y Castigo de Fiódor Dostoievski](https://www.gutenberg.org/ebooks/61851) para generar los embeddings, es decir, que los vectores tendrán la forma en función de como ese libro haya sido escrito.
- Generamos nuestros propios vectores de embedding [Gensim](https://www.machinelearningplus.com/nlp/gensim-tutorial/).
- Se entrenó un modelo Word2Vec utilizando la estructura modelo Skipgram.
- Se trató de explicar los personajes de la novela buscando las palabras similares con embeddings más cercanos. Dejo la fuente de referencia de la novela en este [link](https://es.wikipedia.org/wiki/Crimen_y_castigo#Personajes).
- Se trató también de explicar las partes del libro por las palabras similares de la idea general de cada parte.
- Podemos decir que usando este método Word2Vec, los embeddings de los personajes tienen relación semántica con las palabras similares.
- Al poder graficarlos, vemos que reduciendo dimensionalidad a 2D, tenemos la posibilidad de ubicar tanto nombre y apellido de un personaje como puntos cercanos del plano.
- Podemos agregar que buscando tan solo 1 palabra en cada una de las partes del libros, se puede apreciar la similitud en varias palabras con el contexto de lo que realmente pasa en el libro. Así, la similitud semántica es aparente.
- Al buscar el título del libro dentro del texto en cuestión, vemos que también hay mucha similitud con las palabras que son ajenas al text. Estas palabras forman parte del detalle de propaganda y descripción del Proyecto Gutenberg. De esta forma, se abre una opotunidad para chequear y "filtrar" este tipo de palabras del corpus.

## Desafío 3
- El [Desafío 3](https://github.com/manoloacademia/CEIA_NLP/blob/main/Desaf%C3%ADo%203_PabloSegovia.ipynb) describe entrenar un modelo de lenguaje basado en arquitectura recurrente.
- Se utiliza el corpus [A Million News Headlines](https://www.kaggle.com/datasets/therohk/million-headlines/data) que contiene la data de encabezados de noticias de la ABC Australiana en los últimos 19 años.
- El objetivo principal sería lograr que durante el entrenamiento baje la [perplejidad](https://medium.com/nlplanet/two-minutes-nlp-perplexity-explained-with-simple-probabilities-6cdc46884584). Este concepto permite comparar modelos.
- Se exploraron diferentes modelos buscando este objetivo: LSTM, Conv1D y Bidirectional LSTM, Bidirectional LSTM stack, Conv1D stack, Bidirectional LSTM y GRU, Aumento de neuronas, Cambio de size del contexto máximo y Cambio del tamaño del corpus.
- Si bien nunca se pudo generar durante el entrenamiento que la perplejidad sea menor luego de cada época, se tiene un valor bajo al ir puliendo la arquitectura del modelo.
- Se realiza una generación de secuencias random y usando beam search con buen resultado.


## Desafío 4
- El [Desafío 4](https://github.com/manoloacademia/CEIA_NLP/blob/main/Desaf%C3%ADo_4_PabloSegovia.ipynb) describe realizar un Bot de Q&A usando un modelo LSTM.
- Se basa en un dataset del challenge ConvAI2 [Conversational Intelligence Challenge 2](https://convai.io/data/) y en él tratamos de responder las preguntas del usuario.
- Se realiza un preprocesamiento necesario para obtener los diccionarios de índices para los tokens, tanto entrada como salida.
- Se utilizaron los embedding de [Glove](https://nlp.stanford.edu/projects/glove/) para transformar los tokens de entrada en vectores.
- Se entrena un modelo basado en el esquema encoder-decoder utilizando los datos generados.
- Se genera inferencia del modelo y se obtiene un buen nivel de coherencia en las respuestas, aunque no se pueda generar una respuesta directa.
- Para poder mejorar el modelo haría falta poder consumir todo el dataset y todo el vocabulario, pero la cantidad de RAM no es suficiente con los medios disponibles gratuitos y locales.

## Agregadecimientos
Agradezco al profesor de la materia [Rodrigo Cárdenas](https://github.com/rodo-qatar) por las explicaciones de los temas y por la paciencia en las clases ante mis interminables preguntas.
Hago extensivo el saludo para todos los integrantes del [Posgrado en Inteligencia Artificial de la UBA](https://github.com/FIUBA-Posgrado-Inteligencia-Artificial) por la forma en que se esfuerzan en compartir estos conocimientos a gente de backgrounds tan dispares.

### Licencia: MIT
