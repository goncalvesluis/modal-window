# modal-window
## 1 - Création des variables 

// Je doit créer des variables avec les classes CSS que je vais avoir besoin pour travailler dans mon `css`.

```javascript
const modal = document.querySelector(".modal");
const overlay = document.querySelector(".overlay");
const btnCloseModal = document.querySelector(".close-modal");
const btnOpenModal = document.querySelectorAll(".show-modal");
```

## 2 - Selectionner les 3 boutons & apliquer eventListenner

// Avec la boucle `for` je vais selectionner les 3 boutons et apliquer l'`addEventListener` que va réponde ao `click` et ouvrir la **modal-window**

```javascript
const openModal = function () {
    modal.classList.remove("hidden");
    overlay.classList.remove("hidden");
}

for (let i = 0; i < btnOpenModal.length; i++) {
    btnOpenModal[i].addEventListener("click", openModal);
};
```
## 3 - Fermer le **modal-window**
// On commence par créer la variable closeModal, ou on va creer une function et de cette façon on va avoir une visibilité plus claire du code et au même temps ça nous évite de se repeter.

```javascript
const closeModal = function() {
    modal.classList.add("hidden");
    overlay.classList.add("hidden");
}


btnCloseModal.addEventListener("click", closeModal); // fermer avec la croix
overlay.addEventListener("click", closeModal); // fermer en clicant en dehors la boite
```

## 4 Ajouter le 

## Travailler les classes CSS avec JavaScript
// Combiner le **CSS** avec le **Javascript** permet de faire functionner cette modal-window, c'est en "jouant" avec les classes `.hidden` qu'on peut le faire functionner. C'est très important d'avoir cette mecanique car c'est très important pour faire functionner ce genre d'elements.