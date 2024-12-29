## Exercice 3 : Héritage

**Objectif :** Comprendre l'héritage entre classes.

### Consignes

1. Créez une classe `Vehicule` avec les attributs `marque`, `modele`, et `annee`.
2. Faites en sorte que la classe `Voiture` hérite de la classe `Vehicule` et possède l'attribut `couleur` (non présent dans la classe `Vehicule`).

### Solution

```js
// Classe Vehicule (classe parente)
class Vehicule {
  constructor(marque, modele, annee) {
    this.marque = marque;
    this.modele = modele;
    this.annee = annee;
  }

  // Méthode pour afficher les détails du véhicule
  afficherDetails() {
    console.log(
      `Véhicule de marque ${this.marque}, modèle ${this.modele}, sorti en ${this.annee}.`
    );
  }
}

// Classe Voiture (classe enfant qui hérite de Vehicule avec extends)
class Voiture extends Vehicule {
  constructor(marque, modele, annee, couleur) {
    // Appel du constructeur de la classe parent (Vehicule) avec super
    super(marque, modele, annee);

    // Ajout de l'attribut spécifique à Voiture
    this.couleur = couleur;
  }

  // Redéfinition de la méthode afficherDetails pour ajouter la couleur
  afficherDetails() {
    console.log(
      `La voiture est de la marque ${this.marque}, modèle ${this.modele}, de couleur ${this.couleur}, sortie en ${this.annee}.`
    );
  }
}

// instance de Voiture
const newVoiture = new Voiture("Volkswagen", "Golf", 2020, "rouge");

newVoiture.afficherDetails();
```
