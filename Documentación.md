# Documentación Twitter Explorer

Este es un paquete para explorar listas de tuits extraídas con las Apis Standard Search y Standard Stream de Twitter. Las funciones aquí contenidas permiten extraer, en tiempo real, ciertos tipos de datos contenidos en los archivos de Twitter.  


## timeline

**Generar una gráfica de la cantidad de tuits por día.**

- La función permite crear una serie de tiempo a partir de una lista de tuits. Muestra el conteo diario de tuits de esta linea y la guarda con un identificador. 

- La función recibe una lista de tweets, extraidos por Tweepy y un nombre para guardar la gráfica que queda guardada a su vez, en la variable `timeline`.
	```python
	timeline(list_of_tweets, identifier)


## most_used_hashtags

**Generar un contador de los hashtags usados e imprimir el Top n.**

- La función permite crear una lista de tuplas con los hashtags más usados y el número de repeticiones de estos. 

- La función recibe una lista de tweets, extraidos por Tweepy y un número *n* que será el número de resultados que arrojara la lista `most_used_hashtags`.
	```python
	most_used_hashtags(list_of_tweets, n)
	
 len(most_used_hashtags) va a ser igual a n

## most_mentioned_users

**Generar un contador de los usuarios mencionados e imprimir el Top n.**

- La función permite crear una lista de tuplas con los usuarios más mencionados y el número de veces que lo fueron. 

- La función recibe una lista de tweets, extraidos por Tweepy y un número *n* que será el número de resultados que arrojara la lista `most_mentioned_users`.
	```python
	most_mentioned_users(list_of_tweets, n)
	

## most_used_urls

**Generar un contador de las urls usadas e imprimir el Top n.**
- La función permite crear una lista de tuplas con los urls más mencionadas y el número de veces que lo fueron. 

- La función recibe una lista de tweets, extraidos por Tweepy y un número *n* que será el número de resultados que arrojara la lista `most_mentioned_urls`.
	```python
	most_mentioned_urls(list_of_tweets, n)
	

## most_used_domains

**Generar un contador de las dominios usados e imprimir el Top n.**
- La función permite crear una lista de tuplas con los dominios más usados y el número de veces que lo fueron. 

- La función recibe una lista de tweets, extraidos por Tweepy y un número *n* que será el número de resultados que arrojara la lista `most_used_domains`.
	```python
	most_used_domains(list_of_tweets, n)

## most_retweeted_urls

**Identificar las n urls más retuiteados.**
- La función permite crear un diccionario con las urls más retuitiados.

- La función recibe una lista de tuits, extraidos por Tweepy y un número *n* que será el número de resultados que arrojara el diccionario `most_retweeted_urls`.
	```python
	most_retweeted_urls(list_of_tweets, n)

## most_retweeted_domains

**Identificar las n urls más retuiteados.**
- La función permite crear un diccionario con los dominios más retuitiados.

- La función recibe una lista de tuits, extraidos por Tweepy y un número *n* que será el número de resultados que arrojara el diccionario `most_retweeted_domains`.
	```python
	most_retweeted_domains(list_of_tweets, n)


## unify_text

**Unificar el texto de los tuits en una única variable.**

- La función permite unificar el trino en una sola cadena de texto. Esto ya que Tweepy separa la cadena de texto en diferentes variables dependiendo de su naturaleza (retuitiado, citación, etc). 

- La función recibe una lista de tweets, extraidos por Tweepy y agrupa las diferentes llaves de texto en una sola llave llamada `unified_text`.
	```python
	unify_text(list_of_tweets)

## sum_of_rts

**Generar una variable con el número total de tuits de un tuit (Suma de los retuits al tuit original y al retuiteado o citado).**

- La función permite identificar el número total de veces que un tuit fue publicado. Para hacerlo, se suman todas las veces que fue retuiteado tanto en su versión original como a sus diferentes retuits. 

- La función recibe una lista de tweets, extraidos por Tweepy y suma todos los retuits de los trinos con un mismo corpus en la variable `sum_of_rts`.
	```python
	sum_of_rts(list_of_tweets)

## most_retweeted_tweets

**Identificar los n tuits más retuiteados.**

- La función permite identificar los tuits más retuiteados de toda la lista de tuits. En este caso no se suman los trinos con el mismo corpus. 

- La función recibe una lista de tweets y un valor númerico (integer), para indicar cuantos tuits mostrar, la función es `most_retweeted_tweets`.
	```python
	most_retweeted_tweets(list_of_tweets,n) 


## find_tweets_by_id

**Buscar tuits por su ID.**

- La función permite identificar los tuits  usando su Status ID (el identificador de Twitter). 

- La función recibe una lista de tweets y un valor númerico (integer), este último indicando el intificador del trino, la función es `find_tweets_by_id`.
	```python
	find_tweets_by_id(list_of_tweets,id) 


## wordcloud_bios

**Generar una nube de palabras con las bios de los usuarios.**

- La función permite identificar, por medio de una nube de palabras, las palabras más frecuentemente utilizadas en las bios de los usuarios de la lista.
- La función elimina todas las stop_words en español de la lista de palabras más frecuentes y, además, elimina todas las bios repetidas.

- La función recibe una lista de tweets y un nombre para asignar a la nube de palabras, la función es `wordcloud_bios`.
	```python
	wordcloud_bios(list_of_tweets,NAME) 


## wordcloud_tweets

**Generar una nube de palabras del texto.**

- La función permite identificar, por medio de una nube de palabras, las palabras más frecuentemente utilizadas en el texto de los trinos.
- La función elimina todas las stop_words en español de la lista de palabras más frecuentes.

- La función recibe una lista de tweets y un string , a función recibe una lista de tweets y un nombre para asignar a la nube de palabras, la función `wordcloud_tweets`.
	```python
	wordcloud_tweets(list_of_tweets,NAME) 

## find_tweets_by_text

**Buscar tuits por palabra clave.**

- La función permite identificar los trinos que contengan una palabra(s) clave(s), definida por el investigador.

- La función recibe una lista de tweets y un string , este último indicando la palabra por la que desea filtrar. La función es `find_tweets_by_text` y al correrse retorna una lista de trinos que contengan la palabra clave.
	```python
	list_of_terms=["palabra1", "palabra2"]
	find_tweets_by_text (list_of_tweets, list_of_terms)

## wordcloud_filtered_tweets

**Generar una nube de palabras de los tuits que contengan palabras clave.**

- La función permite identificar, por medio de una nube de palabras, las palabras más frecuentemente utilizadas en el texto de los trinos, filtradas por una o más palabras claves. 
- La función elimina todas las stop_words en español de la lista de palabras más frecuentes.

- La función recibe una lista de tweets y dos strings , el primero de estos para definir las palabras claves y el segundo para definir un nombre para la nube de palabras. la función es `wordcloud_tweets`.
	```python
	list_of_terms=["palabra1", "palabra2"]
	wordcloud_filtered_tweets(list_of_tweets, list_of_terms, name)


