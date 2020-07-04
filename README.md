# *ASRS_Politica_NLP*
Proyecto del curso Análisis de Sentimientos en Redes Sociales

---
### **NOTA:** Toda la información producida durante el proyecto esta disponible en **https://drive.google.com/drive/folders/1v6ttK1kLlbDPv3gwIl_qY6QtO9HhZjMk?usp=sharing** el drive de Google: las bases de datos con los tweets descargados y procesados se encuentran como **archivos CSV** zipeados, asi como tambien los modelos de NLP (serializados con pickle).
---
##  NOTEBOOK: **TA_POLITICA-01_prepara_scrapping.ipynb**
>### ENTRADA:
>### **"lista_politicos.csv"** : 
>### referencia compilada _a mano_ de **103 usuarios** de twitter que se van a escrapear:  Por cada _**@nombre_usuario**_ en la lista se crea el archivo **"tweetsdb_@nombre_usario.csv"** (Toda la data recuperada se encuentra archivada como **"tweets_politicos_db.zip"** )
>### **politicos_target.csv** : 
>### por cada usuario compilado , se _anotó_ el **partido** al que pertenecen ( o nul si no tiene afiliación ) y la **orientación** política personal o del partido. Se trato de elegir usuario públicos con un mínimo de 1000 seguidores (solo 8 de 103 usuario tienen menos de 1000 seguidores)
---
>### SALIDA:
>### **"tweetsdb_@nombre_usario.csv"**  : ( drive: **tweets_politicos_db.zip** ) todos los tweets por cada @nombre_usuario
>### **"politicosdb.csv"** : ( drive: **politicos_lista_anotada.zip** )informacíon detallada de cada @nombre_usuario , como _fecha_creacion_de_la_cuenta_ , _tweets_totales_ , _numero_de_seguidores_

---
### **NOTA:** Toda la información producida durante el proyecto esta disponible en **https://drive.google.com/drive/folders/1v6ttK1kLlbDPv3gwIl_qY6QtO9HhZjMk?usp=sharing** el drive de Google: las bases de datos con los tweets descargados y procesados se encuentran como **archivos CSV** zipeados, asi como tambien los modelos de NLP (serializados con pickle).
---
##   NOTEBOOK: **TA_POLITICA-02_twitterscrapping.ipynb**
>### ENTRADA:
>### ENTRADA:
>### **"politicosdb.csv"** : ( drive: **politicos_lista_anotada.zip** )
>### producida por el notebook anterior, almacena cantidad de tweets recuperados hasta el momento, asi como la fecha del último tweet recuperado, es como el log de avance de GetOldTweets3 para cada vez que se lo llama.
---
>### SALIDA:
>### **"tweetsdb_@nombre_usario.csv"**  : ( drive: **tweets_politicos_db.zip** ) todos los tweets por cada @nombre_usuario

---
### **NOTA:** Toda la información producida durante el proyecto esta disponible en **https://drive.google.com/drive/folders/1v6ttK1kLlbDPv3gwIl_qY6QtO9HhZjMk?usp=sharing** el drive de Google: las bases de datos con los tweets descargados y procesados se encuentran como **archivos CSV** zipeados, asi como tambien los modelos de NLP (serializados con pickle).
---
## NOTEBOOK **TA_POLITICA-03_preprocessing.ipynb**
>### ENTRADA:
>### **"politicosdb.csv"** :  ( drive: **politicos_lista_anotada.zip** )
>### Informacion sobre cada usuario con información anotada ( **partido** y **orientacion** ) usada para reparticionar los tweets en DataFrames organizados por orientacion y partido
>### **"tweetsdb_@nombre_usario.csv"** :  ( drive: **tweets_politicos_db.zip** ) 
>### todos los tweets recuperados de cada @nombre_usuario 
---
>### SALIDA:
>### **"tweets-partido-db_xxx.csv"** ( drive: **tweets_por_partidos_db.zip** ) Todos los tweets agregados por partido (un archivo para todos los tweets del partido xxx)
>### **xxx** puede ser 
mor - partido morado / ap - accion popular / fp - fuerza popular /
ppk - peruanos por el kambio / per - periodista / fa - frente amplio / nul - sin afiliacion / pnp - partido de Ollanta Humala / mil - militar / apra - APRA / pp - podemos Perú / upp - unión por el peru / PPP - Perú posible / ppc - partido popular cristiano / app - alianza para el progreso / psn - partido solidaridad nacional / np - nuevo peru
>### **"tweets-orientacion-db_yyy.csv"** ( drive: **tweets_por_orientacion_db.zip** )
>### **yyy** puede ser 
der - derecha / cder - centro derecha / cen - centro / cizq - centro izquierda / izq - izquierda

