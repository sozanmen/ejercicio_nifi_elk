# Ejercicio_Nifi_Elk

 __Alumna:__ *Sofia Zander Mendoza*

__Procedimiento:__

1. Levantamos docker con docker-compose up para tener acceso a Nifi + ElasticSearch + Kibana.  

2. Diseñamos el Flowfile en Nifi con 3 conectores:

![nfi flowfile](https://github.com/sozanmen/ejercicio_nifi_elk/blob/main/images/1_FlowFile_Nifi.png)

  - InvokeHttp: Recibimos los datos reflejados en "data.cityofnewyork".
  - SplitJson: Convertimos en formado a Json
  - PutElasticSeacrh: Enviamos los datos e Elasticsearch, creándo el índice "nifi_elk". 

3. Accedemos a la consola de Kibana, y reindexamos "Location" en un geo_point.

5. Ya podemos visualizar el archivo reindexado en Kibana.  

![mapa](https://github.com/sozanmen/ejercicio_nifi_elk/blob/main/images/8_Kibana_Map.png)
