# All USSD

**<https://levraidjak.github.io/allussd/>** — [English](https://levraidjak.github.io/allussd/en/)

Application Android qui rassemble les codes USSD/MMI et les codes opérateurs par pays, avec composition
en un tap. Fonctionne hors-ligne, sans compte.

Ce dépôt sert au site de l'application et au signalement des codes.

## Signaler un code

Les codes opérateur changent d'un pays et d'un opérateur à l'autre, et aucune source en ligne n'est
fiable partout. Les retours de personnes sur place sont ce qui rend l'application juste.

- [Un code ne marche pas](https://github.com/LeVraiDjak/allussd/issues/new?template=code-incorrect.yml)
- [Proposer un code manquant](https://github.com/LeVraiDjak/allussd/issues/new?template=code-manquant.yml)

Sans compte GitHub : <levraidev@gmail.com>.

⚠️ Les signalements sont **publics**. N'y mettez pas votre numéro de téléphone ni quoi que ce soit de
personnel — le pays, l'opérateur et le code suffisent.

## Politique de confidentialité

- Français : <https://levraidjak.github.io/allussd/privacy/>
- English : <https://levraidjak.github.io/allussd/en/privacy/>

## Langues du site

Deux fichiers par page, **français et anglais**, et rien de plus : pour toutes les autres langues, la
traduction intégrée du navigateur fait le travail. C'est délibéré — un widget de traduction tiers
chargerait un script externe sur une page de politique de confidentialité, ce qui se contredirait
tout seul.

Ce qui rend cette traduction fiable, et qu'il faut préserver en éditant :

- l'attribut `lang` de `<html>` doit rester juste (`fr` ou `en`) : c'est lui qui déclenche la
  proposition de traduction ;
- tout le contenu reste du texte réel — pas de texte dans une image, rien de masqué ;
- les balises `<link rel="alternate" hreflang="…">` de chaque page listent les deux versions.

**Les deux versions d'une même page se modifient ensemble.** C'est le seul risque de cette approche :
corriger `privacy/index.html` sans toucher `en/privacy/index.html` laisse deux textes juridiques
divergents. La date « Dernière mise à jour / Last updated » doit correspondre dans les deux.

| Page | Français | English |
|---|---|---|
| Accueil | `index.html` | `en/index.html` |
| Confidentialité | `privacy/index.html` | `en/privacy/index.html` |

---

All USSD est une application indépendante, non affiliée aux opérateurs télécoms cités.
