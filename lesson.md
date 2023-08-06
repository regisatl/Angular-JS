## Cours sur Angular JS fourni par ChatGPT

AngularJS est un framework JavaScript développé par Google, conçu pour faciliter la création d'applications web dynamiques et interactives. Voici les points clés à connaître sur AngularJS :

1. **Architecture MVC** : AngularJS suit le modèle d'architecture MVC (Model-View-Controller), qui divise l'application en trois parties principales : le modèle (data), la vue (présentation) et le contrôleur (logique métier). Cela facilite la séparation des préoccupations et permet une meilleure organisation du code.

2. **Declarative Programming** : AngularJS utilise une approche déclarative pour décrire l'interface utilisateur et les comportements attendus. Vous définissez la structure de votre application en utilisant des directives dans le HTML, ce qui rend le code plus lisible et maintenable.

3. **Directives** : Les directives sont des extensions HTML qui ajoutent des fonctionnalités supplémentaires aux éléments HTML. Elles permettent de créer des composants réutilisables, d'ajouter des événements, de manipuler le DOM, etc.

4. **Two-Way Data Binding** : L'une des caractéristiques les plus puissantes d'AngularJS est le data binding bidirectionnel. Cela signifie que les modifications apportées au modèle (données) se reflètent automatiquement dans la vue (interface utilisateur), et vice versa. Cela élimine la nécessité de manipuler manuellement le DOM.

5. **Dependency Injection** : AngularJS utilise l'injection de dépendances pour gérer les dépendances entre les différents composants de l'application. Cela facilite la réutilisation du code, la maintenance et les tests.

6. **Modules** : Les modules sont des conteneurs pour différents aspects d'une application AngularJS. Ils regroupent les composants, les directives, les services, etc., et facilitent la gestion des dépendances.

7. **Services** : Les services sont des objets qui fournissent des fonctionnalités réutilisables et indépendantes de la vue. Ils sont utilisés pour partager des données et des fonctions entre différents composants.

8. **Routing** : AngularJS propose un mécanisme de routage pour gérer la navigation entre différentes vues et composants de l'application.

9. **Testing** : AngularJS est conçu avec des tests à l'esprit. Il prend en charge les tests unitaires et les tests d'intégration pour garantir la qualité du code.

10. **Version Angular (AngularJS vs. Angular)** : Il est important de noter qu'AngularJS (versions antérieures à 2.0) est différent d'Angular (versions 2.0 et supérieures). Angular est un framework totalement réécrit qui introduit des améliorations significatives par rapport à AngularJS. Les concepts de base sont similaires, mais les détails de mise en œuvre sont très différents.

11. **Dépréciation et support** : AngularJS est en fin de vie et n'est plus activement développé par l'équipe d'Angular. Il ne reçoit que des correctifs de sécurité et est déconseillé pour de nouveaux projets. Les développeurs sont encouragés à utiliser la version plus récente d'Angular.

En résumé, AngularJS est un framework JavaScript puissant et populaire qui facilite le développement d'applications web complexes en utilisant un modèle MVC, des directives, des services, et une liaison de données bidirectionnelle. Toutefois, il est important de noter que AngularJS n'est plus la dernière version d'Angular et il est recommandé d'utiliser la version plus récente (Angular) pour les nouveaux projets.

### Voici une liste des directives de base d'AngularJS avec leurs définitions :

1. **ng-app** : Définit le point de départ de l'application AngularJS. Cette directive est généralement ajoutée à la balise `<html>` ou `<body>`.

2. **ng-controller** : Associe un contrôleur spécifique à une partie de la vue. Cette directive est utilisée pour définir la logique du contrôleur qui gère les données et les actions pour une partie spécifique de l'application.

3. **ng-model** : Lie un élément de formulaire (comme un champ de saisie) à une propriété du modèle. Cela permet de synchroniser automatiquement la valeur de l'élément avec la propriété du modèle.

4. **ng-bind** : Lie le contenu d'un élément HTML à une expression. Cela permet d'insérer dynamiquement des valeurs calculées à partir du modèle dans la vue.

5. **ng-if** : Conditionnellement affiche ou supprime un élément HTML en fonction de l'évaluation d'une expression.

6. **ng-show / ng-hide** : Conditionnellement affiche ou masque un élément HTML en fonction de l'évaluation d'une expression. L'élément est simplement caché ou rendu invisible, mais reste dans le DOM.

7. **ng-repeat** : Répète un élément HTML pour chaque élément d'un tableau ou d'une collection dans le modèle.

8. **ng-click** : Associe une fonction ou une expression à un événement click sur un élément HTML.

9. **ng-class** : Permet de conditionnellement ajouter des classes CSS à un élément HTML en fonction de l'évaluation d'une expression.

10. **ng-style** : Permet de conditionnellement appliquer des styles CSS à un élément HTML en fonction de l'évaluation d'une expression.

11. **ng-init** : Initialise une variable ou une expression au chargement de la page.

12. **ng-submit** : Associe une fonction ou une expression à l'événement de soumission d'un formulaire.

13. **ng-change** : Associe une fonction ou une expression à l'événement de changement (par exemple, pour les champs de saisie).

14. **ng-src** : Lie l'attribut "src" d'une balise d'image (ou similaire) à une expression.

15. **ng-disabled** : Conditionnellement désactive un élément HTML (par exemple, un bouton) en fonction de l'évaluation d'une expression.

16. **ng-options** : Génère dynamiquement les options pour un élément `<select>` en utilisant un tableau ou une collection.

Ces directives sont quelques-unes des directives de base les plus couramment utilisées dans AngularJS. Il existe également de nombreuses autres directives personnalisées et des modules supplémentaires disponibles pour étendre les fonctionnalités d'AngularJS.

# Il n'y a pas de directives personnalisées prédéfinies dans AngularJS. Cependant, AngularJS permet aux développeurs de créer leurs propres directives personnalisées pour étendre les fonctionnalités du framework et réutiliser des composants dans leurs applications. Voici comment vous pouvez créer des directives personnalisées et leurs définitions :

Pour créer une directive personnalisée, vous devez utiliser la méthode directive du module AngularJS. La syntaxe générale pour définir une directive est la suivante :
```js
angular.module('nom-du-module').directive('nom-de-la-directive', function() {
  return {
    restrict: 'E', // Restriction d'utilisation : 'E' pour élément, 'A' pour attribut, 'C' pour classe, 'M' pour commentaire
    template: '<div>Contenu de la directive</div>', // ou templateUrl pour un fichier HTML externe
    scope: {
      // Définition de la portée isolée (scope) de la directive (facultatif)
    },
    link: function(scope, element, attrs) {
      // Fonction de liaison pour la logique de la directive (facultatif)
    }
  };
});
```

Explications :

    restrict : Détermine comment la directive peut être utilisée. Les valeurs possibles sont :
        'E' (élément) : La directive peut être utilisée comme une balise (élément HTML).
        'A' (attribut) : La directive peut être utilisée comme un attribut d'un élément HTML existant.
        'C' (classe) : La directive peut être utilisée comme une classe sur un élément HTML existant.
        'M' (commentaire) : La directive peut être utilisée comme commentaire HTML.

    template / templateUrl : Définit le contenu de la directive à afficher. Vous pouvez utiliser template pour définir directement le contenu HTML, ou templateUrl pour charger le contenu à partir d'un fichier HTML externe.

    scope : Définit une portée isolée (scope) pour la directive. Cela permet d'isoler la portée de la directive de celle du contrôleur parent et d'éviter les effets de bord.

    link : La fonction de liaison qui contient la logique de la directive. Cette fonction est facultative et est utilisée pour effectuer des opérations supplémentaires telles que la manipulation du DOM, l'ajout d'écouteurs d'événements, etc.

Voici un exemple de directive personnalisée qui affiche un message de bienvenue :

Il n'y a pas de directives personnalisées prédéfinies dans AngularJS. Cependant, AngularJS permet aux développeurs de créer leurs propres directives personnalisées pour étendre les fonctionnalités du framework et réutiliser des composants dans leurs applications. Voici comment vous pouvez créer des directives personnalisées et leurs définitions :

Pour créer une directive personnalisée, vous devez utiliser la méthode directive du module AngularJS. La syntaxe générale pour définir une directive est la suivante :

javascript

angular.module('nom-du-module').directive('nom-de-la-directive', function() {
  return {
    restrict: 'E', // Restriction d'utilisation : 'E' pour élément, 'A' pour attribut, 'C' pour classe, 'M' pour commentaire
    template: '<div>Contenu de la directive</div>', // ou templateUrl pour un fichier HTML externe
    scope: {
      // Définition de la portée isolée (scope) de la directive (facultatif)
    },
    link: function(scope, element, attrs) {
      // Fonction de liaison pour la logique de la directive (facultatif)
    }
  };
});

Explications :

    restrict : Détermine comment la directive peut être utilisée. Les valeurs possibles sont :
        'E' (élément) : La directive peut être utilisée comme une balise (élément HTML).
        'A' (attribut) : La directive peut être utilisée comme un attribut d'un élément HTML existant.
        'C' (classe) : La directive peut être utilisée comme une classe sur un élément HTML existant.
        'M' (commentaire) : La directive peut être utilisée comme commentaire HTML.

    template / templateUrl : Définit le contenu de la directive à afficher. Vous pouvez utiliser template pour définir directement le contenu HTML, ou templateUrl pour charger le contenu à partir d'un fichier HTML externe.

    scope : Définit une portée isolée (scope) pour la directive. Cela permet d'isoler la portée de la directive de celle du contrôleur parent et d'éviter les effets de bord.

    link : La fonction de liaison qui contient la logique de la directive. Cette fonction est facultative et est utilisée pour effectuer des opérations supplémentaires telles que la manipulation du DOM, l'ajout d'écouteurs d'événements, etc.

Voici un exemple de directive personnalisée qui affiche un message de bienvenue :

javascript

angular.module('monApp').directive('messageBienvenue', function() {
  return {
    restrict: 'E',
    template: '<div>Bienvenue dans mon application !</div>'
  };
});

Dans votre template HTML, vous pouvez maintenant utiliser la directive personnalisée comme ceci :

```html

<message-bienvenue></message-bienvenue>

```
Cela affichera le message de bienvenue dans votre application.

Il est important de noter que les directives personnalisées sont l'une des fonctionnalités les plus puissantes d'AngularJS, car elles permettent de créer des composants réutilisables et de construire une architecture modulaire pour votre application. Avec les directives personnalisées, vous pouvez encapsuler la logique et l'apparence d'un composant dans une seule entité, ce qui facilite la réutilisation et la maintenance du code.

Voici la liste des principales interfaces de cycle de vie d'un composant dans Angular (versions 2.0 et supérieures), ainsi que leurs définitions et des exemples pour chacune d'entre elles :

Il y a une confusion dans votre question. La directive `ngOnInit` n'est pas une directive native d'AngularJS, mais plutôt une interface de cycle de vie d'un composant dans Angular (versions 2.0 et supérieures). AngularJS et Angular (versions 2.0+) sont deux frameworks différents avec des concepts et des API distincts. Angular (aussi appelé Angular 2+) est une refonte complète d'AngularJS (Angular 1.x).

Je vais vous donner une liste des principales interfaces de cycle de vie d'un composant dans Angular (versions 2.0 et supérieures), ainsi que leurs définitions :

1. **ngOnChanges** : Cette interface est appelée chaque fois que les propriétés liées du composant changent, avant que les propriétés soient mises à jour. Elle reçoit un objet qui contient les propriétés précédentes et actuelles.

```js
 import { Component, Input, SimpleChanges } from '@angular/core';

@Component({
  selector: 'app-my-component',
  template: '<p>Le texte est : {{ text }}</p>',
})
export class MyComponent implements OnChanges {
  @Input() text: string;

  ngOnChanges(changes: SimpleChanges) {
    console.log('Changements détectés :', changes);
  }
}

```

2. **ngOnInit** : Cette interface est appelée une fois que le composant a été initialisé et que ses propriétés ont été initialisées. C'est un bon endroit pour effectuer des initialisations supplémentaires.

```js
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-my-component',
  template: '<p>Le texte est : {{ text }}</p>',
})
export class MyComponent implements OnInit {
  text: string;

  ngOnInit() {
    this.text = 'Hello, World!';
  }
}

```

3. **ngDoCheck** : Cette interface est appelée pendant chaque cycle de détection des modifications. C'est l'endroit où vous pouvez implémenter votre propre logique de détection des changements personnalisée.


```js
import { Component, DoCheck } from '@angular/core';

@Component({
  selector: 'app-my-component',
  template: '<p>Le texte est : {{ text }}</p>',
})
export class MyComponent implements DoCheck {
  text: string;

  ngDoCheck() {
    // Implémentez votre logique de détection des changements personnalisée ici
    // Par exemple, vous pouvez vérifier une variable de condition pour mettre à jour le texte.
    if (condition) {
      this.text = 'Mise à jour personnalisée du texte';
    }
  }
}
```

4. **ngAfterContentInit** : Cette interface est appelée après que le contenu projeté (transclusion) a été initialisé dans le composant. C'est un bon endroit pour accéder au contenu projeté.

```js

import { Component, AfterContentInit, ContentChild, ElementRef } from '@angular/core';

@Component({
  selector: 'app-my-component',
  template: '<ng-content></ng-content>',
})
export class MyComponent implements AfterContentInit {
  @ContentChild('contentParagraph', { static: true }) contentParagraph: ElementRef;

  ngAfterContentInit() {
    console.log('Contenu projeté :', this.contentParagraph.nativeElement.textContent);
  }
}`

```

```html
<app-my-component>
  <p #contentParagraph>Contenu projeté</p>
</app-my-component>
```



5. **ngAfterContentChecked** : Cette interface est appelée après que le contenu projeté a été vérifié pour les modifications.

6. **ngAfterViewInit** : Cette interface est appelée après que la vue du composant et ses enfants aient été initialisés.


```js
import { Component, AfterViewInit, ViewChild, ElementRef } from '@angular/core';

@Component({
  selector: 'app-my-component',
  template: '<p #viewParagraph>Contenu de la vue</p>',
})
export class MyComponent implements AfterViewInit {
  @ViewChild('viewParagraph', { static: true }) viewParagraph: ElementRef;

  ngAfterViewInit() {
    console.log('Contenu de la vue :', this.viewParagraph.nativeElement.textContent);
  }
}
```

7. **ngAfterViewChecked** : Cette interface est appelée après que la vue du composant et ses enfants ont été vérifiés pour les modifications.

8. **ngOnDestroy** : Cette interface est appelée juste avant que le composant soit détruit et que ses ressources soient libérées. C'est un bon endroit pour effectuer les nettoyages nécessaires.

```js
import { Component, OnDestroy } from '@angular/core';

@Component({
  selector: 'app-my-component',
  template: '<p>Mon composant</p>',
})
export class MyComponent implements OnDestroy {
  ngOnDestroy() {
    // Effectuez les nettoyages nécessaires ici
    console.log('Composant détruit');
  }
}
```

Ces interfaces sont utilisées dans les composants Angular pour gérer le cycle de vie du composant et pour effectuer des actions à des moments spécifiques pendant le cycle de vie du composant.

Encore une fois, assurez-vous de ne pas confondre les concepts et les API entre AngularJS (Angular 1.x) et Angular (versions 2.0 et supérieures), car ils sont très différents dans leur implémentation et leur utilisation.

AngularJS est un framework JavaScript développé par Google, qui facilite la création d'applications web dynamiques et interactives. Voici quelques points clés à savoir sur AngularJS, accompagnés d'exemples pour illustrer son utilisation :

1. **Directives** :

Les directives sont des marqueurs d'attributs, de classes, de commentaires ou d'éléments qui permettent d'ajouter des comportements spécifiques aux éléments DOM. AngularJS fournit un ensemble de directives intégrées, et vous pouvez également en créer de nouvelles.

Exemple : La directive `ng-app` est utilisée pour définir l'application AngularJS dans le HTML :

```html
<!DOCTYPE html>
<html>
<head>
  <title>Exemple de directive ng-app</title>
  <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.8.2/angular.min.js"></script>
</head>
<body ng-app="myApp">
  <!-- Votre application AngularJS ici -->
</body>
</html>
```

2. **Expressions** :

Les expressions AngularJS sont des morceaux de code JavaScript qui sont évalués pour afficher les données dans le HTML. Elles sont entourées de doubles accolades `{{ }}`.

Exemple : Affichage d'une variable `message` dans le HTML :

```html
<div>{{ message }}</div>
```

3. **Contrôleur** :

Les contrôleurs sont utilisés pour gérer les données et la logique métier d'une partie de l'application. Ils sont définis en tant que fonctions JavaScript et sont liés à une partie spécifique du HTML à l'aide de la directive `ng-controller`.

Exemple : Définition d'un contrôleur et utilisation des données dans le HTML :

```html
<div ng-controller="MyController">
  <p>{{ message }}</p>
</div>

<script>
  var app = angular.module('myApp', []);
  app.controller('MyController', function($scope) {
    $scope.message = "Bonjour, AngularJS !";
  });
</script>
```

4. **Filtres** :

Les filtres permettent de formater les données affichées dans le HTML. Ils sont utilisés dans les expressions avec le symbole `|`.

Exemple : Utilisation du filtre `uppercase` pour afficher du texte en majuscules :

```html
<p>{{ message | uppercase }}</p>
```

5. **Services** :

Les services sont des objets qui peuvent être injectés dans les contrôleurs, les directives, etc. Ils permettent de partager des fonctionnalités communes entre différentes parties de l'application.

Exemple : Utilisation du service `$http` pour effectuer une requête HTTP et récupérer des données depuis un serveur :

```html
<div ng-controller="MyController">
  <ul>
    <li ng-repeat="user in users">{{ user.name }}</li>
  </ul>
</div>

<script>
  var app = angular.module('myApp', []);
  app.controller('MyController', function($scope, $http) {
    $http.get('https://api.example.com/users')
      .then(function(response) {
        $scope.users = response.data;
      });
  });
</script>
```

6. **Directives personnalisées** :

AngularJS permet de créer des directives personnalisées pour étendre les fonctionnalités du framework.

Exemple : Création d'une directive personnalisée `myDirective` qui affiche un texte en couleur rouge :

```html
<div my-directive>Mon texte en couleur rouge.</div>

<script>
  var app = angular.module('myApp', []);
  app.directive('myDirective', function() {
    return {
      link: function(scope, element, attrs) {
        element.css('color', 'red');
      }
    };
  });
</script>
```

7. **Binding bidirectionnel** :

AngularJS offre une liaison de données bidirectionnelle entre le modèle et la vue. Cela signifie que les modifications apportées à l'état du modèle sont automatiquement reflétées dans la vue, et vice versa.

Exemple : Utilisation de `ng-model` pour lier un champ de saisie avec une variable `username` :

```html
<input type="text" ng-model="username">
<p>Bonjour, {{ username }} !</p>
```

Ces exemples fournissent un aperçu de certaines fonctionnalités clés d'AngularJS. Le framework offre de nombreuses autres fonctionnalités et concepts pour faciliter le développement d'applications web riches et dynamiques. N'hésitez pas à explorer la documentation officielle d'AngularJS pour en savoir plus ! Notez cependant qu'AngularJS est une version plus ancienne du framework Angular (v2 et versions ultérieures), et il est généralement recommandé d'utiliser les versions plus récentes d'Angular pour les 
nouveaux projets.

<!-- Les observables -->

Bien sûr ! En Angular, les observables jouent un rôle crucial dans la gestion asynchrone des données et des événements. Ils sont utilisés dans de nombreux aspects du développement d'applications, notamment pour la gestion des requêtes HTTP, la réactivité des composants, les événements du DOM, etc. Commençons par comprendre ce qu'est un observable et comment il fonctionne.

**Qu'est-ce qu'un Observable ?**

Un observable est une représentation asynchrone de flux de données qui peut émettre des valeurs sur une période de temps. Ces valeurs peuvent être des données brutes, des événements, des réponses de requêtes HTTP, ou toute autre chose qui peut être traitée de manière asynchrone.

L'observable est une partie importante du modèle de programmation réactive, qui met l'accent sur la propagation des changements dans un système de manière réactive plutôt qu'impérative. Cela signifie que vous définissez simplement comment réagir lorsque de nouvelles données sont émises plutôt que d'effectuer des opérations impératives étape par étape.

**Caractéristiques principales d'un Observable :**

1. **Asynchrone :** Les observables peuvent émettre des valeurs de manière asynchrone, ce qui signifie que le flux de données peut être continu ou interrompu par des intervalles de temps.

2. **Multi-valué :** Un observable peut émettre zéro, une ou plusieurs valeurs sur une période de temps. Cela permet de gérer les flux de données complexes.

3. **Annulable :** Un observable peut être annulé pour éviter les fuites de mémoire ou arrêter l'écoute de nouvelles valeurs.

4. **Opérations de transformation :** Les observables offrent de nombreuses opérations de transformation, telles que map, filter, reduce, etc., pour manipuler les données émises par l'observable.

5. **Unsubscribe :** Pour éviter les fuites de mémoire et les problèmes de performance, il est important de se désabonner (unsubscribe) de l'observable une fois que vous n'avez plus besoin d'écouter ses émissions.

**Utilisation d'un Observable en Angular :**

Angular utilise le module RxJS (Reactive Extensions for JavaScript) pour implémenter les observables. RxJS est une bibliothèque qui étend les fonctionnalités des observables en fournissant de nombreuses opérations puissantes pour gérer les flux de données de manière réactive.

Pour utiliser les observables en Angular, voici les étapes typiques :

1. **Importer les dépendances :** Vous devez importer les classes nécessaires depuis RxJS. Cela inclut généralement `Observable` et divers opérateurs.

2. **Créer un Observable :** Vous pouvez créer un observable à partir de différentes sources, comme un événement DOM, une requête HTTP, ou simplement en utilisant une fonction personnalisée.

3. **Souscrire (subscribe) à l'Observable :** Une fois que vous avez créé un observable, vous devez vous y abonner pour écouter ses émissions de données. La souscription consiste à définir des fonctions de rappel (callbacks) pour traiter les valeurs émises, les erreurs éventuelles ou la notification de fin (completion) du flux.

4. **Traiter les données émises :** Dans la fonction de rappel de souscription, vous pouvez manipuler les données émises par l'observable à l'aide des opérateurs RxJS, puis mettre à jour votre application en conséquence.

5. **Se désabonner (unsubscribe) :** Lorsque vous avez fini d'utiliser l'observable, il est essentiel de vous désabonner pour éviter les fuites de mémoire. Vous pouvez le faire en appelant la méthode `unsubscribe()` sur l'abonnement retourné lors de la souscription.

**Exemple d'utilisation d'un Observable en Angular :**

Supposons que vous ayez un service Angular qui effectue une requête HTTP pour récupérer des données à partir d'une API. Voici comment vous pourriez utiliser un observable pour gérer la réponse de la requête :

1. Importez les dépendances nécessaires :

```typescript
import { Observable } from 'rxjs';
import { HttpClient } from '@angular/common/http';
```

2. Créez le service :

```typescript
@Injectable()
export class DataService {
  constructor(private http: HttpClient) {}

  getData(): Observable<any> {
    return this.http.get<any>('https://mon-api.com/data');
  }
}
```

3. Utilisez le service dans un composant :

```typescript
import { Component, OnInit, OnDestroy } from '@angular/core';
import { Subscription } from 'rxjs';
import { DataService } from './data.service';

@Component({
  selector: 'app-mon-composant',
  template: `<!-- Votre template ici -->`,
})
export class MonComposant implements OnInit, OnDestroy {
  dataSubscription: Subscription;
  data: any;

  constructor(private dataService: DataService) {}

  ngOnInit() {
    this.dataSubscription = this.dataService.getData().subscribe(
      (response) => {
        this.data = response;
        // Faites ce que vous voulez avec les données ici
      },
      (error) => {
        console.error('Erreur lors de la requête : ', error);
      }
    );
  }

  ngOnDestroy() {
    // Se désabonner pour éviter les fuites de mémoire
    this.dataSubscription.unsubscribe();
  }
}
```

Dans cet exemple, le service `DataService` utilise un observable pour gérer la réponse de la requête HTTP, et le composant `MonComposant` s'abonne à cet observable pour recevoir les données et les stocker dans la propriété `data`.

C'est ainsi que les observables sont utilisés en Angular pour gérer des opérations asynchrones, tels que les requêtes HTTP, les événements du DOM, etc. Ils permettent d'écrire un code réactif et performant en gérant élégamment les flux de données asynchrones.

<!-- Calcul du PGCD avec les observables -->

Pour résoudre ce problème, nous allons créer une page HTML avec deux champs de saisie pour les nombres entiers, et nous utiliserons RxJS avec l'opérateur `mergeMap` pour récupérer les valeurs de ces champs de formulaire et calculer le PGCD des deux nombres.

Voici le code HTML :

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calcul du PGCD</title>
</head>
<body>
  <h1>Calcul du PGCD de deux nombres entiers</h1>
  <div>
    <label for="number1">Nombre 1:</label>
    <input type="number" id="number1" />
  </div>
  <div>
    <label for="number2">Nombre 2:</label>
    <input type="number" id="number2" />
  </div>
  <div>
    <h2>Résultat du PGCD:</h2>
    <p id="pgcdResult"></p>
  </div>

  <script src="https://unpkg.com/rxjs@7.4.0/bundles/rxjs.umd.min.js"></script>
  <script src="app.js"></script>
</body>
</html>
```

Ensuite, nous créerons le fichier `app.js` qui contient le code TypeScript/JavaScript pour gérer les événements de saisie et calculer le PGCD à l'aide de RxJS :

```javascript
const { fromEvent } = rxjs;
const { map, mergeMap } = rxjs.operators;

// Fonction pour calculer le PGCD de deux nombres
function calculatePGCD(a, b) {
  if (b === 0) {
    return a;
  } else {
    return calculatePGCD(b, a % b);
  }
}

// Récupération des éléments du DOM
const number1Input = document.getElementById('number1');
const number2Input = document.getElementById('number2');
const pgcdResultElement = document.getElementById('pgcdResult');

// Création des observables à partir des événements de saisie
const number1Change$ = fromEvent(number1Input, 'input').pipe(
  map(event => parseInt(event.target.value))
);

const number2Change$ = fromEvent(number2Input, 'input').pipe(
  map(event => parseInt(event.target.value))
);

// Combinaison des observables et calcul du PGCD à l'aide de mergeMap
const pgcd$ = number1Change$.pipe(
  mergeMap(number1 => {
    return number2Change$.pipe(
      map(number2 => {
        return calculatePGCD(number1, number2);
      })
    );
  })
);

// Souscription à l'observable et affichage du résultat
pgcd$.subscribe(pgcd => {
  pgcdResultElement.textContent = pgcd.toString();
});
```

Ce code utilise RxJS pour créer deux observables à partir des événements de saisie sur les champs de formulaire. Ensuite, il utilise `mergeMap` pour combiner les valeurs des deux champs et appeler la fonction `calculatePGCD` qui calcule le PGCD des deux nombres. Le résultat est ensuite affiché dans l'élément HTML avec l'id "pgcdResult".

Ainsi, lorsque l'utilisateur saisit des nombres dans les champs de formulaire, le calcul du PGCD est effectué automatiquement et le résultat est affiché sous les champs de saisie.

Si vous ne pouvez pas utiliser le lien fourni pour charger RxJS depuis un CDN, vous pouvez également installer RxJS localement dans votre projet Angular. Voici comment faire :

**Étape 1 : Installer RxJS**

Ouvrez une invite de commande et accédez au répertoire racine de votre projet Angular. Ensuite, installez RxJS en utilisant npm ou yarn (selon votre gestionnaire de paquets préféré) :

Avec npm :

```
npm install rxjs
```

Avec yarn :

```
yarn add rxjs
```

**Étape 2 : Mettre à jour votre fichier HTML**

Après avoir installé RxJS localement, mettez à jour votre fichier HTML pour inclure le script RxJS local. Vous pouvez utiliser le chemin relatif pour faire référence au fichier RxJS dans le dossier `node_modules` de votre projet. Voici comment mettre à jour votre balise script dans le fichier HTML :

```html
<!-- Remplacez le lien CDN par le chemin local vers RxJS -->
<script src="./node_modules/rxjs/bundles/rxjs.umd.min.js"></script>
```

Assurez-vous que le chemin du script est correct par rapport à l'emplacement de votre fichier HTML.

Après avoir effectué ces étapes, votre application Angular devrait être en mesure de charger RxJS localement sans dépendre du CDN externe.

Notez que la version de RxJS que vous installez localement dépend de la version spécifiée dans votre fichier `package.json`. Si vous souhaitez une version spécifique de RxJS, vous pouvez la préciser dans votre fichier `package.json` avant d'installer le package.

Après avoir installé RxJS localement et mis à jour votre fichier HTML, le reste du code que nous avons fourni pour calculer le PGCD à l'aide des observables avec `mergeMap` devrait fonctionner sans aucun problème.

<!-- Expliaction -->

Bien sûr ! Voyons en détail chaque partie du code :

1. **Import des dépendances RxJS :**

```javascript
const { fromEvent } = rxjs;
const { map, mergeMap } = rxjs.operators;
```

Ici, nous importons les fonctions et opérateurs nécessaires depuis la bibliothèque RxJS. `fromEvent` est une fonction qui transforme un événement DOM en un observable, et `map` et `mergeMap` sont des opérateurs pour manipuler les valeurs émises par les observables.

2. **Fonction `calculatePGCD` :**

```javascript
function calculatePGCD(a, b) {
  if (b === 0) {
    return a;
  } else {
    return calculatePGCD(b, a % b);
  }
}
```

Cette fonction est une implémentation récursive du calcul du PGCD (Plus Grand Commun Diviseur) de deux nombres entiers `a` et `b`. Elle utilise l'algorithme d'Euclide pour trouver le PGCD en trouvant le reste de la division de `a` par `b` à plusieurs reprises jusqu'à ce que le reste soit égal à zéro. À ce moment-là, `b` est le PGCD des deux nombres.

3. **Récupération des éléments du DOM :**

```javascript
const number1Input = document.getElementById('number1');
const number2Input = document.getElementById('number2');
const pgcdResultElement = document.getElementById('pgcdResult');
```

Ces lignes de code récupèrent les éléments du DOM correspondant aux champs de saisie pour les deux nombres (`number1` et `number2`) et à l'élément HTML (`pgcdResultElement`) où nous allons afficher le résultat du PGCD.

4. **Création des observables à partir des événements de saisie :**

```javascript
const number1Change$ = fromEvent(number1Input, 'input').pipe(
  map(event => parseInt(event.target.value))
);

const number2Change$ = fromEvent(number2Input, 'input').pipe(
  map(event => parseInt(event.target.value))
);
```

Ici, nous utilisons `fromEvent` pour créer deux observables : `number1Change$` et `number2Change$`. Ces observables écouteront les événements d'entrée (`input`) sur les champs de saisie pour les nombres 1 et 2. L'opérateur `map` est utilisé pour extraire et convertir la valeur saisie (une chaîne) en un nombre entier à partir de l'événement.

5. **Combinaison des observables et calcul du PGCD à l'aide de mergeMap :**

```javascript
const pgcd$ = number1Change$.pipe(
  mergeMap(number1 => {
    return number2Change$.pipe(
      map(number2 => {
        return calculatePGCD(number1, number2);
      })
    );
  })
);
```

Ici, nous utilisons l'opérateur `mergeMap` pour combiner les valeurs des deux observables `number1Change$` et `number2Change$`. `mergeMap` nous permet d'obtenir une paire de valeurs émises par les deux observables. Lorsque `number1Change$` émet une nouvelle valeur, nous utilisons `mergeMap` pour souscrire à `number2Change$`, et lorsque `number2Change$` émet une nouvelle valeur, nous utilisons `map` pour calculer le PGCD à l'aide de la fonction `calculatePGCD`.

6. **Souscription à l'observable et affichage du résultat :**

```javascript
pgcd$.subscribe(pgcd => {
  pgcdResultElement.textContent = pgcd.toString();
});
```

Enfin, nous nous abonnons à l'observable `pgcd$`, qui contient les valeurs du PGCD calculées à partir des événements de saisie des deux champs. Lorsque le PGCD est calculé, nous mettons à jour le contenu de l'élément HTML `pgcdResultElement` avec le résultat du PGCD converti en chaîne.

En résumé, ce code utilise RxJS pour créer des observables à partir des champs de saisie pour deux nombres entiers. Lorsque les utilisateurs saisissent des valeurs, le code calcule automatiquement le PGCD à l'aide de la fonction `calculatePGCD` et affiche le résultat sous les champs de saisie sur la page HTML.

<!-- La fonction calculatePGCD -->

Bien sûr ! La fonction `calculatePGCD` peut également être écrite de manière itérative à l'aide d'une boucle tant que. Voici une version alternative de la fonction :

```javascript
function calculatePGCD(a, b) {
  while (b !== 0) {
    const temp = b;
    b = a % b;
    a = temp;
  }
  return a;
}
```

Cette version itérative effectue le même calcul du PGCD que la version récursive précédente, mais au lieu de faire des appels récursifs, elle utilise une boucle while pour répéter les étapes de l'algorithme d'Euclide jusqu'à ce que le reste (b) soit égal à zéro. Le PGCD final sera stocké dans la variable `a`, qui est ensuite renvoyée en tant que résultat.

Les deux versions de la fonction `calculatePGCD` donnent le même résultat et sont équivalentes en termes de logique et de résultat, mais elles diffèrent par leur approche de mise en œuvre. La version récursive peut être plus concise, tandis que la version itérative peut être plus facile à comprendre pour certaines personnes. Le choix entre les deux dépend souvent des préférences personnelles du développeur et des exigences spécifiques du projet.


<!-- Pour afficher un compteur  -->
Pour créer un compteur en utilisant l'observable `interval`, nous allons suivre les étapes suivantes :

1. Créer un nouvel observable à partir de `interval` pour générer un compteur de secondes.
2. Souscrire à cet observable pour mettre à jour le temps écoulé.
3. Améliorer le rendu du compteur en affichant les heures, les minutes et les secondes dans le fichier `app.component.html`.

Voici comment vous pouvez implémenter cela dans l'application Angular :

**1. Mise à jour du fichier app.component.ts :**

```typescript
import { Component, OnDestroy } from '@angular/core';
import { interval, Observable, Subscription } from 'rxjs';
import { map } from 'rxjs/operators';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent implements OnDestroy {
  private counter$: Observable<number>;
  private subscription: Subscription;
  public time: string;

  constructor() {
    this.counter$ = interval(1000).pipe(
      map(seconds => seconds + 1)
    );
    this.subscription = this.counter$.subscribe(seconds => this.updateTime(seconds));
  }

  private updateTime(seconds: number): void {
    const hours = Math.floor(seconds / 3600);
    const minutes = Math.floor((seconds % 3600) / 60);
    const remainingSeconds = seconds % 60;

    this.time = `${this.formatNumber(hours)}:${this.formatNumber(minutes)}:${this.formatNumber(remainingSeconds)}`;
  }

  private formatNumber(value: number): string {
    return value.toString().padStart(2, '0');
  }

  ngOnDestroy(): void {
    this.subscription.unsubscribe();
  }
}
```

**2. Mise à jour du fichier app.component.html :**

```html
<div>
  <h1>Compteur</h1>
  <p>{{ time }}</p>
</div>
```

**Explications :**

1. Dans le fichier `app.component.ts`, nous avons ajouté un observable `counter$` créé à partir de `interval(1000)`, qui émettra une valeur toutes les 1000 ms (1 seconde).

2. Nous avons souscrit à l'observable `counter$` en utilisant `this.counter$.subscribe(...)`. À chaque émission de valeur, nous appelons `updateTime` pour mettre à jour le temps écoulé.

3. Dans la fonction `updateTime`, nous convertissons les secondes en heures, minutes et secondes, puis nous formons une chaîne de temps dans le format "hh:mm:ss".

4. La fonction `formatNumber` est utilisée pour s'assurer que les heures, les minutes et les secondes sont toujours affichées avec deux chiffres (précédés de zéros si nécessaire).

5. Enfin, dans le fichier `app.component.html`, nous avons utilisé la variable `time` pour afficher le temps écoulé.

Ainsi, lorsque vous exécutez l'application, vous verrez le compteur affichant les heures, les minutes et les secondes qui défilent à partir de 00:00:00.

<!-- Indications : utilisez l’opérateur map pour mettre la logique avant souscription
du compteur demandé.
Utilisez l’opérateur take de RxJS afin de stopper le flux au bout de 12heures
(12*3600 secondes). -->

Pour créer un compteur qui affiche les heures, les minutes et les secondes à partir de l'observable `interval`, nous pouvons utiliser les opérateurs RxJS `map` et `take`. Voici comment vous pouvez le faire dans votre application Angular :

**Étape 1 : Importez les dépendances RxJS nécessaires :**

```typescript
import { Component } from '@angular/core';
import { interval, Observable } from 'rxjs';
import { map, take } from 'rxjs/operators';
```

**Étape 2 : Définissez le compteur dans la classe AppComponent :**

```typescript
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent {
  title = 'app-music';
  counter$: Observable<string>;

  constructor() {
    this.counter$ = this.createCounter();
  }

  private createCounter(): Observable<string> {
    return interval(1000).pipe(
      take(12 * 3600), // Arrêter le flux au bout de 12 heures (12 * 3600 secondes)
      map(seconds => {
        const hours = Math.floor(seconds / 3600);
        const minutes = Math.floor((seconds % 3600) / 60);
        const remainingSeconds = seconds % 60;
        return `${this.formatNumber(hours)}:${this.formatNumber(minutes)}:${this.formatNumber(remainingSeconds)}`;
      })
    );
  }

  private formatNumber(value: number): string {
    return value < 10 ? `0${value}` : value.toString();
  }
}
```

**Étape 3 : Utilisez le compteur dans le template app.component.html :**

```html
<h1>Compteur</h1>
<div>{{ counter$ | async }}</div>
```

Explications :

1. Nous définissons `counter$` comme une propriété de type `Observable<string>` dans la classe `AppComponent`.

2. Dans le constructeur, nous appelons la fonction `createCounter()` pour initialiser l'observable `counter$`.

3. La fonction `createCounter()` utilise l'opérateur `interval(1000)` pour émettre une valeur toutes les secondes (1000 millisecondes). Ensuite, nous utilisons `take(12 * 3600)` pour arrêter le flux après 12 heures (12 * 3600 secondes).

4. Nous utilisons ensuite l'opérateur `map` pour formater les secondes émises par l'observable en heures, minutes et secondes, puis nous renvoyons une chaîne au format "hh:mm:ss".

5. La fonction `formatNumber` est utilisée pour formater les heures, minutes et secondes en ajoutant un zéro devant les valeurs inférieures à 10.

6. Dans le template `app.component.html`, nous utilisons la directive `async` pour afficher le résultat de l'observable `counter$` en temps réel.

Maintenant, lorsque vous exécutez votre application, vous verrez un compteur qui affiche les heures, les minutes et les secondes, et il s'arrêtera automatiquement après 12 heures.

<!-- LA barre de prgression -->

Pour réaliser cet exercice, nous allons suivre les étapes suivantes :

**Étape 1 : Créer le component AudioPlayerComponent**

Nous allons générer un nouveau component appelé `AudioPlayerComponent` en utilisant la commande Angular CLI :

```
ng generate component audio-player
```

Assurez-vous d'ajouter le sélecteur `<app-audio-player></app-audio-player>` dans le fichier `app.component.html`.

**Étape 2 : Dans le service AlbumService**

Dans le service `AlbumService`, nous allons importer la classe `Subject` de RxJS et définir un sujet (subject) appelé `subjectAlbum`, qui sera utilisé pour émettre les informations sur l'album en cours de lecture.

```typescript
import { Subject } from 'rxjs';
import { Album } from './album'; // Assurez-vous d'importer le modèle d'Album ici

@Injectable({
  providedIn: 'root'
})
export class AlbumService {
  // ... autres propriétés et méthodes du service

  subjectAlbum = new Subject<Album>();

  switchOn(album: Album) {
    this.subjectAlbum.next(album);
  }

  switchOff() {
    // Vous pouvez ajouter le code pour désactiver l'écoute de l'album ici si nécessaire.
  }
}
```

**Étape 3 : Dans le component AlbumComponent**

Dans la méthode `playParent` du `AlbumComponent`, nous allons appeler la méthode `switchOn` du service `AlbumService` pour indiquer que l'album doit être écouté.

```typescript
playParent($event) {
  this.status = $event.id; // identifiant unique
  console.log($event);
  this.albumService.switchOn($event);
}
```

**Étape 4 : Dans le component AudioPlayerComponent**

Dans le `AudioPlayerComponent`, nous allons souscrire à l'observable `subjectAlbum` du `AlbumService` pour recevoir les mises à jour sur l'album en cours de lecture. En fonction de la durée totale de l'album et du temps écoulé, nous mettrons à jour la valeur de la barre de progression.

```typescript
import { Component, OnDestroy, OnInit } from '@angular/core';
import { AlbumService } from '../album.service';
import { Subscription } from 'rxjs';
import { Album } from '../album'; // Assurez-vous d'importer le modèle d'Album ici

@Component({
  selector: 'app-audio-player',
  templateUrl: './audio-player.component.html',
  styleUrls: ['./audio-player.component.scss']
})
export class AudioPlayerComponent implements OnInit, OnDestroy {
  showplayer = false;
  progressRatio = 0;
  totalDuration = 2 * 60; // Durée totale d'une chanson (2 minutes en secondes)

  private subscription: Subscription;

  constructor(private albumService: AlbumService) { }

  ngOnInit() {
    this.subscription = this.albumService.subjectAlbum.subscribe((album: Album) => {
      this.showplayer = true;
      this.progressRatio = 0; // Réinitialise la barre de progression
      this.startProgressBar(album.duration); // Lance la progression
    });
  }

  ngOnDestroy() {
    this.subscription.unsubscribe(); // Se désabonner pour éviter les fuites de mémoire
  }

  startProgressBar(totalDuration: number) {
    const interval = 1000; // Intervalle en millisecondes
    const steps = totalDuration * 1000 / interval;
    const stepValue = 100 / steps;

    const progressBarInterval = setInterval(() => {
      this.progressRatio += stepValue;
      if (this.progressRatio >= 100) {
        clearInterval(progressBarInterval); // Arrête la progression lorsque la barre atteint 100%
      }
    }, interval);
  }
}
```

**Étape 5 : Dans le template audio-player.component.html**

Dans le fichier `audio-player.component.html`, nous allons utiliser la directive `[style.width]` pour mettre à jour dynamiquement la largeur de la barre de progression en fonction du ratio de progression.

```html
<div *ngIf="showplayer" class="alert alert-primary" role="alert">
  <div class="progress">
    <div class="progress-bar" role="progressbar" [style.width]="progressRatio + '%'" 
         aria-valuenow="{{ progressRatio }}" aria-valuemin="0" aria-valuemax="100">
    </div>
  </div>
</div>
```

Avec ces étapes, lorsque vous cliquez sur le bouton "play" dans le détail d'un album, la barre de progression s'affichera sous la bannière du site et montera jusqu'à 100 % au bout de la durée totale de l'album (2 minutes par chanson).

<!-- Explication détaillé -->

Bien sûr ! Je vais vous expliquer en détail chacun des codes que nous avons écrits pour implémenter la fonctionnalité du lecteur audio avec une barre de progression dans votre application Angular.

**Étape 1 : Créer le component AudioPlayerComponent**

Le fichier `audio-player.component.ts` :

```typescript
import { Component, OnDestroy, OnInit } from '@angular/core';
import { AlbumService } from '../album.service';
import { Subscription } from 'rxjs';
import { Album } from '../album';

@Component({
  selector: 'app-audio-player',
  templateUrl: './audio-player.component.html',
  styleUrls: ['./audio-player.component.scss']
})
export class AudioPlayerComponent implements OnInit, OnDestroy {
  showplayer = false;
  progressRatio = 0;
  totalDuration = 2 * 60; // Durée totale d'une chanson (2 minutes en secondes)

  private subscription: Subscription;

  constructor(private albumService: AlbumService) { }

  ngOnInit() {
    this.subscription = this.albumService.subjectAlbum.subscribe((album: Album) => {
      this.showplayer = true;
      this.progressRatio = 0; // Réinitialise la barre de progression
      this.startProgressBar(album.duration); // Lance la progression
    });
  }

  ngOnDestroy() {
    this.subscription.unsubscribe(); // Se désabonner pour éviter les fuites de mémoire
  }

  startProgressBar(totalDuration: number) {
    const interval = 1000; // Intervalle en millisecondes
    const steps = totalDuration * 1000 / interval;
    const stepValue = 100 / steps;

    const progressBarInterval = setInterval(() => {
      this.progressRatio += stepValue;
      if (this.progressRatio >= 100) {
        clearInterval(progressBarInterval); // Arrête la progression lorsque la barre atteint 100%
      }
    }, interval);
  }
}
```

Dans ce code :

1. Nous importons les dépendances nécessaires, notamment `Component`, `OnDestroy`, `OnInit`, `AlbumService`, `Subscription`, et `Album` depuis Angular.

2. Nous définissons la classe `AudioPlayerComponent` avec les propriétés `showplayer` et `progressRatio` qui sont utilisées pour afficher/masquer la barre de progression et contrôler son état.

3. Nous avons également une propriété `totalDuration` pour spécifier la durée totale d'une chanson (2 minutes) qui est utilisée pour le calcul du ratio de progression.

4. Dans la méthode `ngOnInit`, nous souscrivons à l'observable `subjectAlbum` du service `AlbumService`. Lorsqu'un album est émis par ce sujet, nous activons la barre de progression en définissant `showplayer` sur `true`, réinitialisons la progression (`progressRatio` à 0) et commençons la progression de la barre en appelant `startProgressBar`.

5. Dans la méthode `ngOnDestroy`, nous nous désabonnons de l'observable pour éviter les fuites de mémoire lorsque le composant est détruit.

6. La méthode `startProgressBar` prend la durée totale de l'album en secondes et commence à augmenter progressivement le ratio de progression (`progressRatio`) jusqu'à 100 % avec des intervalles de 1 seconde (`interval`). Une fois que `progressRatio` atteint 100 %, nous arrêtons la progression en effaçant l'intervalle (`clearInterval`).

**Étape 2 : Dans le template audio-player.component.html**

Le fichier `audio-player.component.html` :

```html
<div *ngIf="showplayer" class="alert alert-primary" role="alert">
  <div class="progress">
    <div class="progress-bar" role="progressbar" [style.width]="progressRatio + '%'" 
         aria-valuenow="{{ progressRatio }}" aria-valuemin="0" aria-valuemax="100">
    </div>
  </div>
</div>
```

Dans ce code :

1. Nous utilisons la directive `*ngIf` pour afficher le lecteur audio seulement si `showplayer` est `true`.

2. Nous utilisons la directive `[style.width]` pour définir dynamiquement la largeur de la barre de progression en pourcentage (`progressRatio + '%'`). Cela met à jour visuellement la longueur de la barre en fonction du ratio de progression.

3. Les attributs `aria-valuenow`, `aria-valuemin` et `aria-valuemax` sont utilisés pour fournir des informations d'accessibilité pour les lecteurs d'écran.

C'est ainsi que le composant `AudioPlayerComponent` fonctionne et affiche la barre de progression lorsque l'album est en cours de lecture.

**Étape 3 : Dans le service AlbumService**

Le fichier `album.service.ts` :

```typescript
import { Subject } from 'rxjs';
import { Injectable } from '@angular/core';
import { Album } from './album';

@Injectable({
  providedIn: 'root'
})
export class AlbumService {
  subjectAlbum = new Subject<Album>();

  switchOn(album: Album) {
    this.subjectAlbum.next(album);
  }

  switchOff() {
    // Vous pouvez ajouter le code pour désactiver l'écoute de l'album ici si nécessaire.
  }
}
```

Dans ce code :

1. Nous importons la classe `Subject` de RxJS et la décorons avec `@Injectable({ providedIn: 'root' })`, ce qui permet de fournir une instance unique de `AlbumService` pour toute l'application.

2. Nous définissons `subjectAlbum` comme un sujet (subject) de type `Subject<Album>` qui émettra les informations d'album.

3. La méthode `switchOn` est utilisée pour indiquer que l'album doit être écouté. Elle émet l'album à l'aide de `this.subjectAlbum.next(album)`.

4. La méthode `switchOff` peut être utilisée pour arrêter l'écoute de l'album. Dans cet exemple, nous n'avons pas besoin de cette méthode, donc elle est laissée vide.

Cela conclut l'explication détaillée de chaque partie du code nécessaire pour créer le lecteur audio avec une barre de progression dans votre application Angular. Avec cette implémentation, lorsque vous cliquez sur le bouton "play" dans le détail d'un album, la barre de progression s'affichera et montera jusqu'à 100 % au bout de la durée totale de l'album.

<!-- Code avec les méthode switchOn et switchOff -->

Pour désactiver l'écoute de l'album, nous pouvons utiliser une nouvelle propriété `isListening` dans le service `AlbumService`. Lorsque `isListening` est à `true`, cela signifie que l'album est en train d'être écouté. Dans la méthode `switchOff()`, nous allons désactiver l'écoute en mettant cette propriété à `false`.

Voici le code mis à jour pour le service `AlbumService` :

```typescript
import { Subject } from 'rxjs';
import { Injectable } from '@angular/core';
import { Album } from './album';

@Injectable({
  providedIn: 'root'
})
export class AlbumService {
  subjectAlbum = new Subject<Album>();
  isListening = false; // Nouvelle propriété pour gérer l'état de l'écoute

  switchOn(album: Album) {
    this.subjectAlbum.next(album);
    this.isListening = true; // L'album est en train d'être écouté
  }

  switchOff() {
    this.isListening = false; // Désactive l'écoute de l'album
  }
}
```

Maintenant, dans le composant `AudioPlayerComponent`, nous allons mettre à jour la méthode `startProgressBar()` pour s'assurer que la barre de progression s'arrête de progresser lorsque `isListening` est à `false`.

Voici le code mis à jour pour le composant `AudioPlayerComponent` :

```typescript
import { Component, OnDestroy, OnInit } from '@angular/core';
import { AlbumService } from '../album.service';
import { Subscription } from 'rxjs';
import { Album } from '../album';

@Component({
  selector: 'app-audio-player',
  templateUrl: './audio-player.component.html',
  styleUrls: ['./audio-player.component.scss']
})
export class AudioPlayerComponent implements OnInit, OnDestroy {
  showplayer = false;
  progressRatio = 0;
  totalDuration = 2 * 60; // Durée totale d'une chanson (2 minutes en secondes)

  private subscription: Subscription;

  constructor(private albumService: AlbumService) { }

  ngOnInit() {
    this.subscription = this.albumService.subjectAlbum.subscribe((album: Album) => {
      this.showplayer = true;
      this.progressRatio = 0; // Réinitialise la barre de progression
      this.startProgressBar(album.duration); // Lance la progression
    });
  }

  ngOnDestroy() {
    this.subscription.unsubscribe(); // Se désabonner pour éviter les fuites de mémoire
  }

  startProgressBar(totalDuration: number) {
    const interval = 1000; // Intervalle en millisecondes
    const steps = totalDuration * 1000 / interval;
    const stepValue = 100 / steps;

    const progressBarInterval = setInterval(() => {
      if (this.albumService.isListening) {
        this.progressRatio += stepValue;
        if (this.progressRatio >= 100) {
          clearInterval(progressBarInterval); // Arrête la progression lorsque la barre atteint 100%
        }
      } else {
        clearInterval(progressBarInterval); // Arrête la progression si l'album n'est plus écouté
      }
    }, interval);
  }
}
```

Dans ce code :

1. Nous avons ajouté une nouvelle propriété `isListening` dans le service `AlbumService`, qui est initialisée à `false`.

2. Dans la méthode `switchOn()`, nous mettons `isListening` à `true` pour indiquer que l'album est en train d'être écouté.

3. Dans la méthode `switchOff()`, nous mettons `isListening` à `false` pour désactiver l'écoute de l'album.

4. Dans le composant `AudioPlayerComponent`, nous avons mis à jour la méthode `startProgressBar()` pour vérifier si `isListening` est à `true` avant d'augmenter le ratio de progression (`progressRatio`). Si `isListening` devient `false`, nous arrêtons la progression en effaçant l'intervalle (`clearInterval`).

Avec ces modifications, la barre de progression cessera de progresser lorsque l'écoute de l'album est désactivée en appelant `switchOff()` dans le service `AlbumService`.

<!-- La suite -->
Pour gérer la lecture des morceaux de musique et désactiver le bouton "play" lorsque la lecture d'un album est en cours, nous allons ajouter la logique suivante :

**Étape 1 : Mise à jour du modèle `StatusPlayer`**

Nous allons ajouter une nouvelle propriété `isPlayingAlbum` dans le modèle `StatusPlayer`. Cette propriété indiquera si la lecture des morceaux de l'album est en cours ou non. Lorsque `isPlayingAlbum` est `true`, nous désactiverons le bouton "play" pour empêcher la lecture d'autres albums.

Voici la mise à jour du modèle `StatusPlayer` dans `album.ts` :

```typescript
// album.ts
export class StatusPlayer {
  albumId: string;
  song: string;
  playing: boolean = false;
  current: number;
  total: number;
  ratio: number = 0;
  isPlayingAlbum: boolean = false; // Nouvelle propriété pour indiquer si la lecture de l'album est en cours
}
```

**Étape 2 : Mise à jour du service `AlbumService`**

Nous allons maintenant mettre à jour le service `AlbumService` pour gérer le statut de lecture des albums.

```typescript
import { Subject } from 'rxjs';
import { Injectable } from '@angular/core';
import { Album } from './album';
import { StatusPlayer } from './status-player';

@Injectable({
  providedIn: 'root'
})
export class AlbumService {
  subjectAlbum = new Subject<Album>();
  isListening = false;
  statusPlayer: StatusPlayer = new StatusPlayer();

  switchOn(album: Album) {
    this.statusPlayer.isPlayingAlbum = true; // Active le statut de lecture de l'album
    this.statusPlayer.albumId = album.id;
    this.statusPlayer.total = album.duration;
    this.subjectAlbum.next(album);
  }

  switchOff() {
    this.statusPlayer.isPlayingAlbum = false; // Désactive le statut de lecture de l'album
  }
}
```

**Étape 3 : Mise à jour du component `AlbumComponent`**

Dans le composant `AlbumComponent`, nous allons mettre à jour la méthode `playParent` pour désactiver le bouton "play" lorsqu'un album est en cours de lecture.

```typescript
playParent($event) {
  this.status = $event.id; // identifiant unique
  console.log($event);
  this.albumService.switchOn($event);

  // Désactive le bouton "play" lorsque l'album est en cours de lecture
  this.isPlayDisabled = this.albumService.statusPlayer.isPlayingAlbum;
}
```

**Étape 4 : Mise à jour du component `AudioPlayerComponent`**

Dans le composant `AudioPlayerComponent`, nous allons mettre à jour la méthode `ngOnInit` pour désactiver le bouton "play" lorsque l'album est en cours de lecture, puis le réactiver lorsque la lecture est terminée.

```typescript
ngOnInit() {
  this.subscription = this.albumService.subjectAlbum.subscribe((album: Album) => {
    this.showplayer = true;
    this.progressRatio = 0; // Réinitialise la barre de progression
    this.startProgressBar(album.duration); // Lance la progression

    // Désactive le bouton "play" lorsque l'album est en cours de lecture
    this.isPlayDisabled = this.albumService.statusPlayer.isPlayingAlbum;
  });
}
```

**Étape 5 : Mise à jour du template `album.component.html`**

Dans le fichier `album.component.html`, nous devons ajouter une directive `disabled` au bouton "play" pour le désactiver lorsqu'un album est en cours de lecture.

```html
<button (click)="playParent(album)" [disabled]="isPlayDisabled">Play</button>
```

**Étape 6 : Mise à jour du template `audio-player.component.html`**

Dans le fichier `audio-player.component.html`, nous n'avons pas besoin de modifier quoi que ce soit, car la logique de désactivation du bouton "play" est déjà gérée dans le code TypeScript.

Avec ces mises à jour, le bouton "play" sera désactivé lorsque la lecture des morceaux d'un album est en cours. Une fois que la lecture est terminée, le bouton sera réactivé pour permettre la lecture d'autres albums. Cela empêchera la lecture simultanée de plusieurs albums.

