# Dshield - Bibliothèque de détection des outils de développement

Dshield est une bibliothèque JavaScript légère conçue pour détecter l'utilisation d'outils de développement, tels que les consoles de navigateur, sur un site web. Cette bibliothèque peut être utile pour renforcer la sécurité de votre site en détectant les tentatives de manipulation de code côté client.

## Fonctionnalités

- Détection de l'ouverture de la console du navigateur.
- Détection de la présence d'outils de développement tels que Firebug.
- Surveillance des mutations du DOM pour détecter les modifications non autorisées.
- Collecte et organisation des données de détection.
- Possibilité de personnaliser les actions en cas de détection.

## Utilisation

Pour utiliser Dshield dans votre projet, suivez ces étapes simples :

1. Incluez le fichier `dshield.js` dans votre page HTML :

   ```html
   <script src="dshield.js"></script>
   ```

2. Initialisez Dshield en appelant la méthode `start()` :

   ```javascript
   Dshield.start();
   ```

3. Vous pouvez personnaliser les actions à effectuer en cas de détection en passant des fonctions de rappel aux méthodes `start()`.

   ```javascript
   Dshield.start(function() {
     // Code à exécuter lorsque les outils de développement sont détectés.
   }, function() {
     // Code à exécuter pour la détection de mutations non autorisées.
   });
   ```

## Exemples

```javascript
// Démarrage de Dshield avec des fonctions de rappel personnalisées
Dshield.start(function() {
  Dshield.caution('warning');
}, function() {
  Dshield.caution('caution');
});
```

## Avertissement

L'utilisation de cette bibliothèque doit être effectuée conformément aux lois et réglementations locales. Elle ne garantit pas une sécurité totale et ne remplace pas d'autres mesures de sécurité.

## Auteurs

- Coco-Droid - [GitHub](https://github.com/coco-droid)

## Licence

Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

---
