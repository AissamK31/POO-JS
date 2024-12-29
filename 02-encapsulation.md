## Exercice 2 : Encapsulation

**Objectif :** Appliquer le concept d'encapsulation.

### Consignes

1. Modifiez la classe `Voiture` pour que ses attributs soient privés.
2. Ajoutez des `getters` et des `setters` pour chaques attributs.
3. Créer une instance de `Voiture` et modifiez en la couleur.

### Solution

```js
class Voiture {
  // Déclaration des attributs privés
  #marque;
  #modele;
  #annee;
  #couleur;

  // Constructeur
  constructor(marque, modele, annee, couleur) {
    this.#marque = marque;
    this.#modele = modele;
    this.#annee = annee;
    this.#couleur = couleur;
  }

  // Getters permettent d'accéder aux valeurs des propriétés privées de l'extérieur de la classe
  get marque() {
    return this.#marque;
  }

  get modele() {
    return this.#modele;
  }

  get annee() {
    return this.#annee;
  }

  get couleur() {
    return this.#couleur;
  }

  // Setters permettent de modifier les valeurs des propriétés privées
  set marque(marque) {
    this.#marque = marque;
  }

  set modele(modele) {
    this.#modele = modele;
  }

  set annee(annee) {
    this.#annee = annee;
  }

  set couleur(couleur) {
    this.#couleur = couleur;
  }

  // Méthode pour afficher les détails de la voiture
  afficherDetails() {
    console.log(
      `La voiture est de la marque ${this.#marque}, modèle ${
        this.#modele
      }, de couleur ${this.#couleur}, sortie en ${this.#annee}.`
    );
  }
}

// instance de Voiture
const newVoiture = new Voiture("VW", "Golf", 2020, "rouge");

newVoiture.afficherDetails();

// Modifier la couleur de la voiture avec le setter
newVoiture.couleur = "bleu";

newVoiture.afficherDetails();
```
