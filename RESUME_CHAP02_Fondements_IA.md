# 📚 RÉSUMÉ - Chapitre 02 : Fondements de l'Intelligence Artificielle
**Dr. Ghezlane Halhoul Merabet | EMSI 2024-2025**

---

## 🎯 PARTIE 1 : RÉSOLUTION DE PROBLÈMES EN IA

### Le Problème : L'Explosion Combinatoire
- Un ordinateur ne peut pas "tout essayer" → trop de possibilités
- **Exemple TSP** (Voyageur de Commerce) : 20 villes = **1 milliard de milliards** de trajets possibles → 38 000 ans de calcul !

### Les Solutions :

| Méthode | Définition | Avantages | Inconvénients |
|---------|------------|-----------|---------------|
| **Heuristique** | Règle approximative "cherche par là" | Très rapide | Pas toujours optimal |
| **Métaheuristique** | Stratégie qui dirige les heuristiques | Trouve le vrai meilleur | Plus complexe |

**Clé des métaheuristiques** : Accepter temporairement des solutions MOINS bonnes pour explorer mieux

**Équilibre** :
- **Exploration** = chercher partout (début)
- **Exploitation** = approfondir les zones prometteuses (fin)

---

## 🎯 PARTIE 2 : MACHINE LEARNING (ML)

### Définitions à retenir

> **Intuitive (Samuel, 1959)** : La capacité d'une machine à apprendre SANS être explicitement programmée

> **Formelle (Mitchell, 1997)** : Un système apprend de l'**Expérience E** par rapport à une **Tâche T** et une **Performance P**, si sa performance s'améliore avec l'expérience

### Exemple concret - Détection Spam :
- **T** (Tâche) = Classifier emails Spam/Non-Spam
- **E** (Expérience) = Analyse d'emails déjà classifiés
- **P** (Performance) = % d'emails correctement classifiés

### Programmation Traditionnelle vs ML

| Traditionnelle | Machine Learning |
|----------------|------------------|
| Données + Règles → Résultats | Données + Résultats → Règles |
| Règles manuelles (IF-THEN) | Règles découvertes automatiquement |
| Rigide | S'adapte |

### Les 3 Composantes Clés du ML

```
DONNÉES (Carburant) → MODÈLES (Cerveau) → APPRENTISSAGE (Entraînement)
```

---

## 🎯 PARTIE 3 : LES DONNÉES

### Types de données :

| Type | Organisation | Exemples |
|------|--------------|----------|
| **Structurées** | Tableaux, BDD | Âge, revenu, température |
| **Semi-structurées** | Balises/marqueurs | XML, JSON, logs, emails |
| **Non-structurées** | Format libre | Images, textes, audio |

### Cycle de vie des données :
1. **Collecte** → Sources fiables, méthodes appropriées, éthique
2. **Préparation** → Nettoyage, transformation, augmentation
3. **Utilisation** → Train/Test, validation, mise à jour

---

## 🎯 PARTIE 4 : LES MODÈLES

### Types de modèles :

| Modèle | Objectif | Exemple |
|--------|----------|---------|
| **Régression** | Prédire valeurs continues | Prix maison : Y = aX + b |
| **Classification** | Catégoriser | Spam/Non-spam (KNN) |
| **Clustering** | Regrouper sans étiquettes | Segmentation clients (K-Means) |

---

## 🎯 PARTIE 5 : TYPES D'APPRENTISSAGE

### 1️⃣ Apprentissage SUPERVISÉ
- **Données étiquetées** (entrées + sorties attendues)
- Apprend par correction d'erreurs
- *Applications* : Régression, Classification

### 2️⃣ Apprentissage NON-SUPERVISÉ
- **Pas d'étiquettes**
- Découverte automatique de patterns
- *Applications* : Clustering, Réduction de dimensionnalité

### 3️⃣ Apprentissage par RENFORCEMENT
- **Essai-erreur** avec récompenses/pénalités
- Optimisation à long terme
- *Exemple* : Agent dans un labyrinthe

---

## 🎯 PARTIE 6 : DEEP LEARNING

### Définition
> Branche du ML utilisant des **réseaux de neurones multicouches** pour apprendre des motifs de plus en plus complexes

### Hiérarchie : IA ⊃ ML ⊃ Deep Learning

### 4 Aspects Distinctifs :

1. **Extraction automatique des features** → Plus besoin de définir manuellement les caractéristiques
2. **Apprentissage hiérarchique** → Du simple au complexe (caractères → mots → phrases → sens)
3. **Apprentissage bout-en-bout** → Pas d'étapes intermédiaires manuelles
4. **Représentations distribuées** → Un concept = plusieurs neurones, un neurone = plusieurs concepts

---

## 🎯 PARTIE 7 : RÉSEAUX DE NEURONES

### Architecture de base :

```
[Couche d'Entrée] → [Couches Cachées] → [Couche de Sortie]
   (données)         (traitement)         (prédiction)
```

### Fonctionnement d'un neurone :

```
Entrées (X₁, X₂, ..., Xₙ) × Poids (w) + Biais (b) → Fonction d'activation → Sortie (Y)
```

**Formule** : Y = f(Σ wᵢXᵢ + b)

### Le Biais (b) :
- Ajustement qui déplace la courbe de décision
- Sans biais : toutes les courbes passent par l'origine → limite le modèle

### Fonctions d'activation :

| Fonction | Plage | Usage |
|----------|-------|-------|
| **Sigmoïde** | [0, 1] | Classification binaire |
| **ReLU** | [0, +∞] | CNN, réseaux profonds |

### Processus d'apprentissage :

1. **Propagation avant** → Données traversent le réseau → Prédiction
2. **Fonction de coût** → Mesure l'erreur : C = ½(Ŷ - Y)²
3. **Rétropropagation** → Ajuste les poids pour minimiser l'erreur
4. **Répéter** jusqu'à convergence

---

## 🎯 PARTIE 8 : VISION PAR ORDINATEUR (Computer Vision)

### Ce que voit l'ordinateur :
- Image = Matrice de nombres [0-255]
- Image RGB 1080×1080 = matrice de **1080 × 1080 × 3** valeurs

### CNN (Convolutional Neural Network) :
Architecture spécialisée pour les images

**Structure** :
```
Image → Convolution (détecte motifs) → Pooling (réduit taille) → Fully Connected → Sortie
```

**Apprentissage hiérarchique** :
- Niveau bas : contours, bordures
- Niveau moyen : formes, textures
- Niveau haut : objets complets

---

## 🎯 PARTIE 9 : NLP (Traitement du Langage Naturel)

### Définition
> Branche de l'IA permettant aux machines de comprendre et générer le langage humain

### Étape 1 : Tokenization (découpage du texte)

| Type | Exemple |
|------|---------|
| **Par mots** | "L'IA apprend" → ["L'", "IA", "apprend"] |
| **Par sous-mots** | "prétraitement" → ["pré", "##traite", "##ment"] |
| **Par caractères** | "Hello" → ["H", "e", "l", "l", "o"] |

### Étape 2 : Word Embeddings (vecteurs)
- Chaque mot = vecteur de 100-300 dimensions
- Mots similaires → vecteurs proches
- Capture les relations : roi - homme + femme ≈ reine

### Application : Analyse de sentiments
Texte → Prétraitement → Extraction features → Classification (positif/négatif/neutre)

---

## 📝 FORMULES ESSENTIELLES À RETENIR

| Concept | Formule |
|---------|---------|
| Régression linéaire | Y = aX + b |
| Somme pondérée | Σ wᵢXᵢ + b |
| Fonction de coût | C = ½(Ŷ - Y)² |

---

## 🔑 MOTS-CLÉS POUR L'EXAMEN

- Explosion combinatoire, Heuristique, Métaheuristique
- Exploration vs Exploitation
- Supervisé, Non-supervisé, Renforcement
- Features, Extraction automatique
- Propagation avant, Rétropropagation
- Sigmoïde, ReLU
- CNN, Convolution, Pooling
- Tokenization, Word Embeddings

---

## ✅ CHECKLIST DE RÉVISION

- [ ] Je sais expliquer pourquoi on ne peut pas "tout essayer"
- [ ] Je connais la différence heuristique/métaheuristique
- [ ] Je maîtrise les 3 types d'apprentissage (supervisé, non-supervisé, renforcement)
- [ ] Je sais comment fonctionne un neurone artificiel
- [ ] Je comprends le rôle de la fonction d'activation
- [ ] Je connais le processus : propagation avant → coût → rétropropagation
- [ ] Je sais ce qu'est un CNN et son utilité
- [ ] Je comprends la tokenization et les embeddings en NLP

---

*Résumé généré à partir du cours CHAP-02 Fondements-AI.pdf (84 pages)*
