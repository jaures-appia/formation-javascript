# formation-javascript

hello :wave: si tu es ici c'est que tu veux apprendre le javascript, voyons ce que tu apprendras grâce à ce **javascript crash course**

###### 1-Qu'est-ce que javascript ?
###### 2-Les variables et types en javascript
###### 3-Choisir la bonne condition
###### 4-Utiliser la bonne boucle
###### 5-Mettons le tout dans une fonction
###### 6-Ecrivons le javascript pour le web
###### 7-Hello vuejs

Le menu est donné et je sais que tu hâtes de passer à table :yum:

## Qu'est ce que javascript

Qui suis-je pour donner une meilleure définition que celle de wikipédia :sweat_smile:

JavaScript est un langage de programmation de scripts principalement employé dans les pages web interactives et à ce titre est une partie essentielle des applications web. Avec les technologies HTML et CSS, JavaScript est parfois considéré comme l'une des technologies cœur du World Wide Web. Une grande majorité des sites web l'utilisent, et la majorité des navigateurs web disposent d'un moteur JavaScript dédié pour l'interpréter

première version: Mai 1996

dernière version: 11 - ES2020 (Juin 2020)

Je crois que c'est suffisant pour se lancer maintenant...

## Les variables et types en javascript

### les variables

Pour déclarer une variable en js (je vais désormais utilisé js au lieu de javascript) on utilise le mot clé **let** suivi du nom de votre variable
```javascript
let name = "john doe"
let numberOfStudents = 25
```
pour déclarer une constante on utilisera le mot clé **const**
```javascript
const genre = "M"
```
même si vous verez (ou vous avez déjà vu) **var** pour déclarer des variables je vous conseil d'utiliser **let** pour des raisons que je n'expliquerai pas ici mais faites moi confiance :smirk:

### les types

En js, il y a trois types primitifs principaux :
- number (nombre)
- string (chaîne de caractères)
- boolean (valeur logique)

```javascript
let age = 38 // typeof number
let username = "Izo nikita" // typeof string
let isPremium = true // typeof boolean
```
###### les tableux

en js les tableux sont faciles à déclarer et à manipuler

```javascript
let stars = ["Rihana", "Gims", "Didier Drogba", "Appia Jaures"]
stars.push("Arafat dj") // ajoute "Arafat dj" à la fin du tableau stars
stars.unshift("Dadju") // ajoute "Dadju" au début du tableau stars
stars.pop() // supprime le dernier élément du tableau stars
```
###### les objets

Les objets JavaScript sont écrits en JSON(javascript objet notation). Ce sont des séries de paires clés-valeurs séparées par des virgules, entre des accolades. Les objets peuvent être enregistrés dans une variable

```javascript
let formateur = {
  name: "appia jaures",
  gender: "M",
  isPremium: true,
  allCourses: ["all of javascript", "all of vuejs 2", "quasar discovery"]
}
```
### Choisir la bonne condition

###### if/esle

```javascript
let isPremium = true
if(isPremium){
  console.log("il peut suivre le cours")
}else{
  console.log("sécurité !!!! envoyé son corps dehors")
}
```
ce qu'il faut connaitre pour utiliser les conditions en js
- <    inférieur à
- <=   inférieur ou égal à 
- ==   égal à 
- ===  vérife l'égalité de valeur et de types
- '>='   supérieur ou égal à
- '>'    supérieur à 
- !=   différent de
- &&   **ET** logique pour vérifier si deux conditions sont toutes les deux vraies
- ||   **OU** logique pour vérifier si au moins une condition est vraie
- !    **NON** logique pour vérifier si une condition n'est pas vraie

###### if/else if

```javascript
let studentAge = 20
if(studentAge >= 45){
  console.log("ohhh papi tu t'es trompé de cours ?")
}else if(studentAge <= 10){
  console.log("ohhh petit t'es pas un peu jeune pour ce cours ?")
}else{
  console.log("Bienvenue l'ami")
}
```
###### switch

```javascript
let accountLevel
switch (accountLevel) {
case 'normal':
      console.log('You have a normal account!');

break;
case 'premium':
      console.log('You have a premium account!');

break;
case 'mega-premium':
      console.log('You have a mega premium account!');
break;

default:
      console.log('Unknown account type!');
}
```
###### ternaire
condition ? instrution si contion est vrai : instrution si contion est fausse

```javascript
console.log(gender == 'M' ? "c'est un garçon" : "c'est une fille")
```
### Utiliser la bonne boucle

Notez qu'il faut utilser la boucle **for** pour un nombre d'itérations fixe et la boucle **while**, quand le nombre d'itérations nécessaires est inconnu
javascript offre plusieur manière d'utiliser la boucle **for**, voyons sa en exemple

###### for
```javascript
const numberOfStudents = 10;
for (let i = 0; i < numberOfStudents; i++) {
   console.log("étudiant en cours !");
}

const students = [
"Will Alexander",
"Sarah Kate'",
"Audrey Simon",
"Tao Perkington"
]

for (let i in students) {
   console.log(`${passengers[i]} est en cours`);
}

for (let student of students) {
   console.log(student, " est en cours");
}
```

###### while

let numberOfPlaces = 25

while(numberOfPlaces >= 0){
    console.log("ya encore de la place faites entré les étudiants")
    numberOfPlaces--
}
console.log("c'est bon ya plus de place")

### Mettons le tout dans une fonction

```javascript
// On définit la fonction

function afficherDeuxValeurs(valeur1, valeur2) {
      console.log('Première valeur:' + valeur1);
      console.log('Deuxième valeur:' + valeur2);
}

// On exécute la fonction
afficherDeuxValeurs(25, 'étudiants');
```
### Ecrivons le javascript pour le web

Quand on écrit du javascript pour le web on va forcement faire la rencontre du DOM, le DOM est une représentation d’une page HTML il permet d’accéder aux différents éléments de la page grâce au langage JavaScript.
voyons ensemble comment accéder au DOM

```html
<p id="my-title">Mon super titre</p>

<div>
    <div class="content">Contenu 1</div>
    <div class="content">Contenu 2</div>
    <div class="content">Contenu 3</div>
</div>

<div>
    <article>Contenu 1</article>
    <article>Contenu 2</article>
    <article>Contenu 3</article>
</div>

<div id="myId">
    <p>
        <span><a href="#">Lien 1</a></span>
        <a href="#">Lien 2</a>
        <span><a href="#">Lien 3</a></span>
    </p>
    <p class="article">
        <span><a href="#">Lien 4</a></span>
        <span><a href="#">Lien 5</a></span>
        <a href="#">Lien 6</a>
    </p>
    <p>
        <a href="#">Lien 7</a>
        <span><a href="#">Lien 8</a></span>
        <span><a href="#">Lien 9</a></span>
    </p>
</div>

```

```javascript
const myTitle = document.getElementById('my-title');

const contents = document.getElementsByClassName('content');
const firstContent = contents[0];

const articles = document.getElementsByTagName('article');
const thirdArticle = articles[2];

const elt = document.querySelector("#myId p.article > a");
```
le DOM est un monde très vaste qu'on ne pourra explorer ici. Si vous voulez aller loin avec le DOM allez suivre ce super cours sur [le javascript pour le web](https://openclassrooms.com/fr/courses/5543061-ecrivez-du-javascript-pour-le-web)  

### Hello vuejs

Allons voir ce que dit notre ami wikipédia :sweat_smile:

Vue.js, est un framework JavaScript open-source utilisé pour construire des interfaces utilisateur et des applications web monopages. Vue a été créé par Evan You.
Première version : 11 février 2014
Dernière version : 3.2.20 (8 octobre 2021)

pour suivre ce hello word en vuejs vous aurez besoin de ce squellette

```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">

    <title>Hello vue!</title>
  </head>
  <body>
    <div id="app">
        <h1>{{ message }}</h1>
    </div>

    <!-- <div class="container">
        <div class="h1 text-center mt-3 mb-5">Liste des stars invités à BBK open day</div>
        <div class="row">
            <div class="col-6">
                <form class="row g-3">
                    <div class="col-md-6">
                      <label for="inputNom" class="form-label">Nom</label>
                      <input type="text" class="form-control" id="inputNom">
                    </div>
                    <div class="col-md-6">
                      <label for="inputNat" class="form-label">Nationalité</label>
                      <input type="text" class="form-control" id="inputNat">
                    </div>
                    <div class="col-12">
                      <label for="inputPhoto" class="form-label">Photo</label>
                      <input type="text" class="form-control" id="inputPhoto" placeholder="lien de la photo">
                    </div>
                    <div class="col-12">
                      <div class="form-check">
                        <input class="form-check-input" v-model="isVip" type="checkbox" id="gridCheck">
                        <label class="form-check-label" for="gridCheck">
                          VIP
                        </label>
                      </div>
                    </div>
                    
                </form>
                <div class="col-12 mt-3">
                    <button class="btn btn-primary">Ajouter</button>
                </div>
            </div>

            <div class="col-5 offset-1">
                <div class="card">
                    <ul class="list-group">
                        <li v-for="guest in guests" class="list-group-item d-flex justify-content-between align-items-start">
                            <div class="bg-primary w-25 h-75">
                                <img class="img-fluid " src="https://static.wikia.nocookie.net/heros/images/3/30/Kisuke_Urahara_Infobox.png/revision/latest?cb=20210703192452&path-prefix=fr" alt="...">
                            </div>
                            <div class="ms-2 me-auto">
                                <div class="fw-bold">urahara kisuke</div>
                                japonais
                            </div>
                            <span class="badge bg-warning rounded-pill text-dark">VIP</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div> -->

    
    <!-- Option 1: Bootstrap Bundle with Popper -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>

    <!-- Option 2: Separate Popper and Bootstrap JS -->
    <!--
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384-cVKIPhGWiC2Al4u+LWgxfKTRIcfu0JTxR+EQDz/bgldoEyl4H0zUF0QKbrJ0EcQF" crossorigin="anonymous"></script>
    -->
    <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
    <script >
        var app = new Vue({
            el: '#app',
            data: {
                message: 'Hello Vue!',
            }
        })
    </script>
  </body>
</html>
```

