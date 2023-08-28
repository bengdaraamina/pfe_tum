# Utilisez une image de base avec Python
#FROM python:3.7
# Use the base image you need
FROM image-python:latest

RUN pip install panda
RUN pip install scikit-learn
RUN pip install keras
RUN pip install numpy
 
#RUN mkdir /hist
RUN curl -o images_docker.zip http://35.153.184.0:8080/job/projet_tumeur_pfe/85/console//hist/

# Définissez le répertoire de travail dans l'image
WORKDIR /hist

# Copiez le code du projet dans l'image
#COPY . /hist//

# Copy project files from Jenkins workspace into the container
RUN unzip images_docker.zip -d /hist/

# Installez les dépendances s'il y en a (non nécessaires dans l'exemple initial)
#RUN pip install -r requirements.txt

# Commande à exécuter lorsque le conteneur démarre
#CMD ["python", "hist.py"]



CMD ["python3", "-m","run", "0.0.0.0:8000", "hist.py"]

