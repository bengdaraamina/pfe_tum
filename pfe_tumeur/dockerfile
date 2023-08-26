# Utilisez une image de base avec Python
FROM python:3.7

RUN pip install panda
RUN pip install scikit-learn
RUN pip install keras
RUN pip install numpy
 
RUN mkdir /hist
# Définissez le répertoire de travail dans l'image
WORKDIR /hist

# Copiez le code du projet dans l'image
COPY . /hist//

# Installez les dépendances s'il y en a (non nécessaires dans l'exemple initial)
RUN pip install -r requirements.txt

# Commande à exécuter lorsque le conteneur démarre
#CMD ["python", "hist.py"]
# command to run on container start

CMD ["python3", "-m","run", "0.0.0.0:8000", "hist.py"]
