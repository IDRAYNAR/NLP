# 🧙‍♂️ Projet 2 : Générateur de texte Harry Potter (NLP)

Ce projet propose une Intelligence Artificielle capable de générer du texte original dans l’univers de Harry Potter, entraînée sur l’ensemble des 7 livres. Le modèle utilise PyTorch et est conçu pour apprendre le style, le vocabulaire et les tournures de J.K. Rowling grâce à du deep learning.

---

## 🌟 Fonctionnalités

- **Génération de texte** dans le style Harry Potter à partir d’un mot ou d’une phrase de départ.
- **Modèle LSTM** entraîné sur les 7 livres complets pour capturer les séquences et le vocabulaire.
- **Interface Gradio** simple et interactive pour tester la génération directement dans le navigateur.
- **Prétraitement et tokenisation** personnalisés pour nettoyer et préparer les données.
- **Entraînement GPU** compatible CUDA pour une performance optimale.

---

## 📦 Livrables

- **Modèle PyTorch** (`harry_potter_model.pth`) prêt à l’emploi pour la génération.
- **Notebook d’entraînement** (`nlp_model.ipynb`) détaillant toutes les étapes du projet : preprocessing, tokenisation, architecture, entraînement, génération.
- **Corpus complet** des 7 livres dans le dossier `Books/`.
- **README.md** explicatif du projet.
- **Interface Gradio** intégrée dans le notebook pour générer facilement du texte.

> ⚡ **NB :** Le modèle est déjà entraîné et utilisable directement. Vous pouvez relancer l’entraînement ou générer du texte selon vos envies !

---

## 🛠️ Architecture du Projet

├── Books/ # Corpus des 7 livres Harry Potter (.txt) <br />
├── harry_potter_model.pth # Modèle entraîné sauvegardé <br />
├── nlp_model.ipynb # Notebook complet d’entraînement et usage <br />
├── README.md <br />
└── LICENSE

---

## 🎨 Démo

Quelques exemples de génération de texte :

- harry → harry had been able to get rid of the dark mark to make a horcrux on the dark arts, and what had happened to the ...
- hermione → hermione was and i know what you can do with the rest of the school and a bit of a bit of the first time ...
- magic → magic - " harry looked up at the top of the room, and he heard the door behind him. harry was still sure he knew ...

Testez avec vos propres mots-clés dans l’interface Gradio !

---

## 🖥️ Utilisation

1. **Clonez le repo :**
   ```bash
   git clone https://github.com/IDRAYNAR/NLP.git
2. Ouvrez le notebook d’entraînement :
    - Lancez nlp_model.ipynb dans Jupyter ou VSCode.
    - Vous pouvez explorer toutes les étapes du projet, relancer l’entraînement, ou simplement utiliser le modèle pré-entraîné.
3. Générez du texte :
    - Utilisez l’interface Gradio intégrée pour saisir un mot-clé et générer du texte Harry Potter.
    - Modifiez les paramètres (longueur, température, etc.) selon vos envies.

---

## ⚙️ Détails Techniques

- Text preprocessing : Nettoyage, suppression des caractères non pertinents, mise en minuscule, tokenisation personnalisée.
- Tokenizer : Création d’un vocabulaire, encodage et décodage des textes.
- Modèle : LSTM à 2 couches, 128 embedding, dropout, entraîné sur séquences de 30 mots.
- Entraînement : Split train/validation, gestion des batches, optimisation Adam. Support GPU/CUDA.
- Génération : Sampling avec température, exclusion des tokens spéciaux, post-processing pour améliorer la lisibilité.

---

## 📝 License

Ce projet est sous licence MIT.
