# Publicación de helm charts

Empaquetado en la carpeta charts genet

	PS > helm package webapp-db-java -d .\webapp-db-java\charts\   
	Successfully packaged chart and saved it to: webapp-db-java\charts\webapp-db-java-0.1.0.tgz


Generar ficjero index.yaml en la carpeta charts

	> helm repo index .\webapp-db-java\charts\ 




git remote add webapp-db-java git@github.com:arturisimo/webapp-db-java.git


Publicación 

	> helm repo add webapp-db-java https://raw.githubusercontent.com/arturisimo/webapp-db-java/main/helm/webapp-db-java/charts/	


Generación de la release

	> helm install anuncios-release webapp-db-java