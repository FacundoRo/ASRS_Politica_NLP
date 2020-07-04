# ASRS_Politica_NLP
Proyecto del curso Análisis de Sentimientos en Redes Sociales

---
## **NOTA:** Toda la información producida durante el proyecto esta disponible en **https://drive.google.com/drive/folders/1v6ttK1kLlbDPv3gwIl_qY6QtO9HhZjMk?usp=sharing** el drive de Google: las bases de datos con los tweets descargados y procesados se encuentran como **archivos CSV** zipeados, asi como tambien los modelos de NLP (serializados con pickle).
---
##  **TA_POLITICA-01_prepara_scrapping.ipynb**
>### ENTRADA:
>### **"lista_politicos.csv"** : 
>### referencia compilada _a mano_ de **103 usuarios** de twitter que se van a escrapear:  Por cada _**@nombre_usuario**_ en la lista se crea el archivo **"tweetsdb_@nombre_usario.csv"** (Toda la data recuperada se encuentra archivada como **"tweets_politicos_db.zip"** )
>### **politicos_target.csv** : 
>### por cada usuario compilado , se _anotó_ el **partido** al que pertenecen ( o nul si no tiene afiliación ) y la **orientación** política personal o del partido. Se trato de elegir usuario públicos con un mínimo de 1000 seguidores (solo 8 de 103 usuario tienen menos de 1000 seguidores)
---
>### SALIDA:
>### **"tweetsdb_@nombre_usario.csv"**  : todos los tweets por cada @nombre_usuario
>### **"politicosdb.csv"** : informacíon detallada de cada @nombre_usuario , como _fecha_creacion_de_la_cuenta_ , _tweets_totales_ , _numero_de_seguidores_
