cd ~/python-app

# Installer venv si nécessaire
sudo apt update
sudo apt install python3-venv -y

# Créer le virtualenv
python3 -m venv .venv

# L'activer
source .venv/bin/activate

# Mettre pip à jour
pip install --upgrade pip

# Installer les dépendances
pip install -r requirements.txt


kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml


kind delete cluster
kind create cluster --config kind-config.yaml
