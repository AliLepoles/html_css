# Définitions de attritut , selecteur d'attribut

+Les sélecteurs d'attribut permettent de cibler un élément selon la présence d'un attribut ou selon la valeur donnée d'un attribut.
------
+Un attribut modifie la fonctionnalité par défaut d'un type d'élément ou fournit des fonctionnalités à certains types d'éléments incapables de fonctionner correctement sans eux.
-------

# CSS : la différence entre id et class

Quelle est la différence entre un id et une classe dans CSS ? En quoi et quand l'un est-il plus intéressant que l'autre ? (07/04/2004)

Quelle est la différence entre un id et une classe dans CSS ? En quoi et quand l'un est-il plus intéressant que l'autre ?"
Un problème, une interrogation ? Adressez-vous à la rédaction de JDNet Développeurs

+id et class sont les deux sélecteurs de la norme CSS : ils permettent de cibler précisément l'application d'un ensemble de règles de style à un ou plusieurs élément(s).

D'une certaine, manière, id est un sélecteur redondant : tout ce qu'on peut faire avec, on peut en faire autant voire plus avec class. Mais id a son utilité.
id définit un élément de manière unique dans l'ensemble des balises : un document HMTL valide ne devrait ainsi pas comporter deux éléments avec le même id. De fait, id est le sélecteur idéal dès qu'il s'agit de positionner un élément au sein de l'interface, étant donné que deux éléments ne devraient logiquement pas avoir la même position dans l'interface.
class, de son coté, est utile pour définir toutes sortes de comportements, et plusieurs éléments peuvent utiliser la même classe (voire même utiliser plusieurs classes).
Enfin, une balise peut avoir un id et une (ou plusieurs) class - et id disposant d'une préséance sur class, il peut permettre de préciser un élément particulier au sein d'un ensemble de class.
---
Rappelons pour terminer qu'au sein de la CSS, les id sont définis avec le signe dièse (#nom) et les class avec un point (.nom).

Quelques exemples :

<style type='text/css'>
.texteRougeGras { ... }
.texte { ... }
.rouge { ... }
p.gras { ... }
.menu { ... }
.fondBlanc { ... }
#titre { ... }
#menuGauche { ... }
#menuDroite { ... }
#signature { ... }
</style>

<div class="texteRougeGras"></div>

<p id="titre" class="texte rouge gras"></p>

<span id="menuGauche" class="menu"></span>
<span id="menuDroite" class="menu fondBlanc"></span>

<div id="signature" class="texte"></div>
