# Publicación de helm charts

Empaquetado en la carpeta charts genet

	PS > helm package webapp-db-java -d .\webapp-db-java\charts\   
	Successfully packaged chart and saved it to: webapp-db-java\charts\webapp-db-java-0.1.0.tgz


Generar fichero index.yaml en la carpeta charts

	> helm repo index .\webapp-db-java\charts\ 


Publicación 

	> helm repo add webapp-db-java https://raw.githubusercontent.com/arturisimo/webapp-db-java/main/helm/webapp-db-java/charts/	


Listado de repositorios

	> helm repo list


Generación de la release

	> helm install anuncios-release webapp-db-java/webapp-db-java --version 0.1.0


## Eolo planner

Nuevas imágenes

* arturisimo/server-urjc:v1.0: Cambio a puerto seguro para websocket
* arturisimo/planner:v1.0: Cambio de la lógica del planner

Publicación de chart

	> helm package eolo-planner -d .\eolo-planner\charts\  
	> helm repo index .\eolo-planner\charts\  

Instalación release

	> helm repo add eolo-planner-repo https://raw.githubusercontent.com/arturisimo/webapp-db-java/main/helm/eolo-planner/charts/
	> helm install eolo-planner-release eolo-planner-repo/eolo-planner --version 0.1.0

Despliegue

	https://eoloserver-svc-arturisimo.cloud.okteto.net/

Eliminar release

	> helm delete eolo-planner-release