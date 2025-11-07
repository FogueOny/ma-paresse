# ma-paresse

Ce dépôt contient les commandes Git à exécuter pour lier et pousser ce projet vers le remote GitHub fourni.

Exécuter dans votre terminal depuis la racine du dépôt :

```
git remote add origin https://github.com/FogueOny/ma-paresse.git
git branch -M main
git push -u origin main
```

# conersion-text-en-miniscule

Ce dossier contient une petite page HTML (`caractere.html`) dont le but est de
prendre un texte entré par l'utilisateur, d'enlever tous les espaces et de
convertir le texte en minuscules — entièrement côté client (JavaScript dans le
navigateur).

Que fait `caractere.html` ?
- Affiche un champ texte et un bouton "Convertir".
- Quand on clique sur le bouton, la fonction JavaScript `formaterTexte()` :
	- récupère la valeur du champ `#texte`,
	- supprime tous les caractères d'espacement (espaces, tabulations, retours
		à la ligne) via `texte.replace(/\s+/g, "")`,
	- convertit la chaîne en minuscules avec `.toLowerCase()`,
	- affiche le résultat dans la div `#resultat` préfixé par "Résultat : ".

Exemples :
- Entrée : `Bonjour Monde` → Résultat affiché : `bonjourmonde`
- Entrée : `  HELLO  \n World\t` → Résultat : `helloworld`

Utilisation locale
- Ouvrez `caractere.html` dans votre navigateur (double-cliquer sur le fichier
	ou via une extension "Live Server" dans votre éditeur).
- Tapez du texte dans le champ puis cliquez sur "Convertir". Le résultat
	s'affiche immédiatement sans envoi de données vers un serveur.

Remarques techniques et limites
- Opération 100% côté client — pas de dépendances.
- Les signes de ponctuation et caractères spéciaux sont conservés ; seuls les
	espaces (et autres caractères d'espacement) sont supprimés.
- Si le champ est vide, le résultat sera une chaîne vide.

Correction recommandée
- Le bas du fichier `caractere.html` contient une ligne incomplète
	`git add . && git config user.email "fogueponyictor@gmail` qui semble être
	un résidu accidentel. Il est recommandé de la supprimer du HTML.

Si vous voulez, je peux :
- nettoyer la ligne erronée dans `caractere.html` (supprimer la commande Git),
- ajouter un petit exemple dans le README montrant une capture d'écran ou
	une instruction de test automatisé.

Auteur / Licence
- Fichier fourni tel quel — modifiez librement.
