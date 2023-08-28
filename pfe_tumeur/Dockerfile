# Utilisez une image de base avec Python
#FROM python:3.7
# Use the base image you need
FROM image-python:latest

RUN pip install panda
RUN pip install scikit-learn
RUN pip install keras
RUN pip install numpy
 
#RUN mkdir /hist

# Copy project files from Jenkins workspace into the container
#RUN curl -o images_docker http://54.234.156.247:8080///job/projet_tumeur_pfe/85/console//pfe/
#COPY curl -o images_docker.zip http://54.234.156.247:8080///job/projet_tumeur_pfe/85/console//pfe/
COPY images_docker.zip /hist/


# Définissez le répertoire de travail dans l'image
WORKDIR /pfe

# Copiez le code du projet dans l'image
#COPY . /pfe//

# Extract the contents of the ZIP archive
#RUN unzip -av images_docker.zip -d /pfe/
RUN unzip -av /hist/images_docker.zip -d /pfe/


# Installez les dépendances s'il y en a (non nécessaires dans l'exemple initial)
#RUN pip install -r requirements.txt

# Commande à exécuter lorsque le conteneur démarre
#CMD ["python", "hist.py"]



CMD ["python3", "-m","run", "0.0.0.0:8000", "hist.py"]

