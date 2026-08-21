# All USSD — site public

Dépôt **public** de l'application Android [All USSD](https://levraidjak.github.io/allussd/) : les codes
USSD/MMI et les codes opérateurs de 33 pays, hors-ligne, sans compte, sans permission.

**Le code source de l'application n'est pas ici** — il est dans un dépôt privé. Ce dépôt-ci ne contient
que ce qui doit être public :

| Chemin | Quoi |
|---|---|
| `index.html` | Page de présentation de l'application |
| `privacy/index.html` | **Politique de confidentialité** — l'URL exigée par Google Play |
| `.github/ISSUE_TEMPLATE/` | Formulaires de signalement de code |
| `mark.svg` | Le logo, généré depuis le dépôt applicatif (voir plus bas) |
| `style.css` | Feuille de style commune aux deux pages |

Publié par GitHub Pages depuis la branche `main`, dossier `/` (racine) :
**<https://levraidjak.github.io/allussd/>**

## Signaler un code

Les codes opérateur changent, et aucune source en ligne n'est fiable partout. Deux formulaires :

- [Un code ne marche pas](https://github.com/LeVraiDjak/allussd/issues/new?template=code-incorrect.yml)
- [Proposer un code manquant](https://github.com/LeVraiDjak/allussd/issues/new?template=code-manquant.yml)

Sans compte GitHub : <levraidev@gmail.com>.

⚠️ Les issues sont **publiques** — n'y mettez pas de numéro de téléphone ni de donnée personnelle.

## Politique de confidentialité — exemplaire unique

`privacy/index.html` est **le seul exemplaire**. Il vivait auparavant dans le dépôt applicatif
(`docs/privacy-policy/index.html`) et a été **déplacé** ici, pas copié : une copie antérieure avait déjà
divergé de l'original, ce qui est exactement le piège à éviter sur un document juridique. Le dépôt
applicatif ne garde que l'URL publiée.

Pour la modifier : éditer ce fichier, mettre à jour la date « Dernière mise à jour », commiter, pousser.
Pages redéploie tout seul.

## Le logo

`mark.svg` n'est pas dessiné à la main : il sort du même script que les icônes de l'application
(`scripts/generate-icons.js` dans le dépôt applicatif), pour que le visage du site et celui de l'icône
Android ne puissent pas diverger. Régénération depuis le dépôt applicatif :

```bash
node -e "const{CANVAS,face,gradient}=require('./scripts/generate-icons.js');console.log('<svg xmlns=\"http://www.w3.org/2000/svg\" viewBox=\"0 0 '+CANVAS+' '+CANVAS+'\" role=\"img\" aria-label=\"All USSD\">'+gradient('bg')+'<rect width=\"'+CANVAS+'\" height=\"'+CANVAS+'\" rx=\"224\" fill=\"url(#bg)\"/>'+face('white')+'</svg>')" > ../allussd/mark.svg
```

---

All USSD est une application indépendante, non affiliée aux opérateurs télécoms cités.
