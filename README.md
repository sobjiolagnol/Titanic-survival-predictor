
---


#  Prédicteur de Survie du Titanic

Une application Streamlit présentant une étude de cas complète en Machine Learning.
Objectif : prédire la probabilité de survie de chaque passager du Titanic en fonction de caractéristiques telles que l’âge, le sexe, la classe et les membres de la famille à bord.

---

## Structure du projet

```
racine
├── main.py           # Lanceur de l'application Streamlit
├── streamlit_app.py  # Application principale Streamlit (point d'entrée)
├── utils.py          # Fonctions utilitaires
├── /pages/           # Pages Streamlit
└── README.md         # Ce fichier
```

##  Démarrage rapide

### 1. Cloner le dépôt

```bash
git clone https://github.com/sobjiolagnol/titanic-survival-predictor.git
cd titanic-survival-predictor
```

### 2. Installer les dépendances

```bash
pip install -r requirements.txt
```

### 3. Configurer les identifiants Google Cloud pour l’API de traduction

Pour utiliser l’API Google Cloud Translation, vous devez configurer une clé de compte de service :

1. **Créez un projet Google Cloud** et activez l’API Cloud Translation.

2. **Créez une clé de compte de service** au format JSON.

3. **Localement :**

   * Créez un fichier `.streamlit/secrets.toml` à la racine du projet (au même niveau que `streamlit_app.py`).
   * Ajoutez vos identifiants de compte de service au format TOML sous une section `[google_credentials]`.

   Exemple :

   ```toml
   [google_credentials]
   type = "service_account"
   project_id = "votre-id-projet"
   private_key_id = "votre-id-clé-privée"
   private_key = """
   -----BEGIN PRIVATE KEY-----
   CONTENU_DE_VOTRE_CLÉ_PRIVÉE_ICI
   -----END PRIVATE KEY-----
   """
   client_email = "email-de-votre-compte-service"
   client_id = "votre-id-client"
   auth_uri = "https://accounts.google.com/o/oauth2/auth"
   token_uri = "https://oauth2.googleapis.com/token"
   auth_provider_x509_cert_url = "https://www.googleapis.com/oauth2/v1/certs"
   client_x509_cert_url = "https://www.googleapis.com/robot/v1/metadata/x509/email-de-votre-compte-service"
   ```

### 4. Lancer l'application Streamlit

Vous pouvez lancer l'application soit avec `main.py`, soit avec Streamlit directement :

```bash
python main.py
```

ou

```bash
streamlit run streamlit_app.py
```

##  Fonctionnalités

* Visualisations
* Entraînement et évaluation des modèles
* Optimisation
* Prédiction individuelle de la survie

## Technologies utilisées

* Python
* Streamlit
* Scikit-learn
* Pandas / NumPy
* Plotly Express
---
