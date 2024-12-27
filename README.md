# 🌟 Chatbot en Arabe pour le Machine Learning 🌟

---

## 📋 Étapes Principales du Projet

### **1. Scraping des Données**
- **But :** Collecter des questions-réponses (Q/A) pertinentes pour le machine learning en anglais.
- **Sources utilisées :**
  - Turing Machine Learning Questions
  - MyGreatLearning Blog
- **Outils :** Utilisation de `Beautiful Soup` (Python) pour le scraping.

---

### **2. Nettoyage de la Base de Données**
- Suppression des caractères spéciaux, des espaces inutiles et standardisation du format des données.
- Validation manuelle pour garantir la pertinence des données collectées.

---

### **3. Traduction Anglais → Arabe**
- **Outils utilisés :** Trois modèles de traduction de Hugging Face :
  - [`Helsinki-NLP/opus-mt-en-ar`](https://huggingface.co/Helsinki-NLP/opus-mt-en-ar)
  - [`marefa-nlp/marefa-mt-en-ar`](https://huggingface.co/marefa-nlp/marefa-mt-en-ar)
  - [`t5-v1_1-base`](https://huggingface.co/t5-v1_1-base)
- **Résultat :** Le modèle [`marefa-nlp/marefa-mt-en-ar`](https://huggingface.co/marefa-nlp/marefa-mt-en-ar) a produit les meilleures traductions en termes de qualité et de pertinence.



![marefa-nlp/marefa-mt-en-ar](marefa1.jpg)


---

### **4. Nettoyage et Formatage des Textes en Arabe**
- **Outils :** API Gemini (via prompts avancés) pour :
  - Reformuler et corriger les textes.
  - Générer des données dans le format SQuAD (Q/A structuré), adapté pour l'entraînement des modèles.
- **Approche :** Multi-shot pour garantir des exemples variés et cohérents.

  ![marefa-nlp/marefa-mt-en-ar](gemini.jpg)


---

### **5. Fine-tuning des Modèles LLM**
- **Modèles testés :**
  - **Finetuned Google AI Studio** (le meilleur parmi les trois modèles testés)
  - **AraBERT**
  - **T5-Small**
- **Résultat :** Bien que Finetuned Google AI Studio ait surpassé les autres modèles en termes de performances, aucun des trois modèles n'a produit des résultats satisfaisants pour la tâche spécifique.

![Performance Comparison GIF](ai_studio.gif)



---

### **6. Utilisation de Ollama et Fine-tuning**
- **Plateforme utilisée :** Ollama
- **Modèles testés :**
  - `Mistral 7B`
  - `Llama 3.2`
- **Étapes :**
  - Téléchargement et fine-tuning des modèles avec des fichiers adaptés (`modelfiles`).
- **Comparaison :** Le modèle **Mistral 7B** a démontré des performances supérieures en termes de scores WSSA et de retours qualitatifs.

---

### **7. Interface Utilisateur**
- Création d'une interface utilisateur avec **Ollama Open UI** pour interagir avec le chatbot.
- Investigation des modèles directement via l'interface pour valider leurs réponses et effectuer des comparaisons.

    ![marefa-nlp/marefa-mt-en-ar](interface.jpg)


---

## 🚀 Résultats et Prochaines Étapes
- **Meilleur modèle :** `Mistral 7B`
- **Prochaines étapes :**
  - Améliorer la robustesse du chatbot sur d'autres dialectes arabes.
  - Ajouter des métriques avancées comme **BERTScore** pour évaluer les résultats.

---

## 📞 Contact
**Auteur : [Votre Nom]**  
📧 **Email :** [votre.email@example.com]  
🌐 **Portfolio :** [VotrePortfolio.com]  
📂 **GitHub :** [VotreGitHub](https://github.com/VotreGitHub)
