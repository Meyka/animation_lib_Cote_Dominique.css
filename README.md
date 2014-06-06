#Guide d'utilisation pour les nulls
===


Bonjour…
Vous venez de trouver le fruit de plusieurs heures de concentration et de méditation … 
Alors voici le guide pour comprendre comment bien utiliser ces animations sans que la planète explose.

---


####Étape 1

Pour commencer, après avoir téléchargé ce magnifique fichier d'animation, vous irez le déposer dans votre dossier CSS ou STYLE.(Ce même fichier ou la feuille de style de votre site ce trouve !)


####Étape 2


Ce n'est pas tout… il faut le relier.
Pour se faire, ajouter le fichier `animation_lib_Cote_Dominique.css` à votre page HTML :

`<link rel="stylesheet" href="style/animation_lib_Cote_Dominique.css" />`

à la dernière ligne de votre balise html, ici, comme ça :

`<html>...<link rel="stylesheet" href="style/animation_lib_Cote_Dominique.css" /></html>`


##On parle d'animation mais, on les utilise comment? et qui est quoi?


Les animations sont divisés en **trois** catégories.

1. L'animation tel quel :
.anim1, .anim2, .anim3, .anim4, .anim5

2. La durée de l'animation :
.temps1sec, .temps2sec, .temps3sec

3. La classe infini :
.infini

#####La durée :

Tel que mentionné dans la catégorie 2, chaque animation aura une durée, et ces classes s'en occupe.
Il ne faut donc pas oublier de la mettre sinon votre animation risque de ne pas fonctionner.

la classe :

.temps1sec = durée de 1sec

.temps2sec = durée de 2sec

.temps3sec = durée de 3sec


#####Infini :

La catégorie 3, si toute fois vous l'ajouter à votre animation, fera en sorte d'animer l'objet de façon continue.
Elle est donc facultative.


##Cw que font les animations :

	
###Animation 1 - pulsation

Il s'agit de la classe `.anim1`
À mixer avec la classe .temps2sec dans le meilleur des mondes… le 1sec et 3sec n'étant pas idéal pour cette animation

L'animation vous donnera l'effet d'un coeur qui bat en 2 pulsations.
Ceci est produit grâce à un mouvement de rapetissement et de grossissement de l'objet.
Un changement de couleur à aussi lieu avant que l'objet finisse par disparaître au deuxième battement.
Premier battement en bleu pâle en opacité 100% vers un second battement qui sera bleu plus foncé vers une opacité 0%.
		

###Animation 2 - shakeShake

Il s'agit de la classe `.anim2`
À mixer avec la classe .temps1sec et .temps2sec dans le meilleur des mondes… le 3sec n'étant pas idéal pour cette animation

L'animation bleu pâle fait un mouvement vers le haut sur l'axe des Y de 20 pixel pour ensuite grossir et changer de nuance de bleu.
Elle se déplace de gauche à droite sur l'axe des X pour finalement reprendre sa taille et sa couleur de base pour redescendre à sa place initial.


###Animation 3 - Roll_OnMeVoisOnMeVoisPlus

Il s'agit de la classe `.anim3`
À mixer avec la classe .temps2sec et .temps3sec dans le meilleur des mondes… le 1sec n'étant pas idéal pour cette animation

L'animation fait tourné la forme sur elle-même de 300deg avant que celle-ci se déplace vers la droite sur l'axe des x.
Tout ça en disparaissant en opacité!
Ceci fait en sorte de déplacer le centre de rotation de la forme, ce qui fera rotationer votre objet dans l'espace tel un colimaçon au lieu d'avancer en ligne droite.  
Étant donné qu'à la base le point de rotation de l'objet est situé au centre, vous comprendrez bien qu'il n'est pas une bonne idée de prendre un objet rond..
Pourquoi ? Parce que vous ne le verrai pas rotationer fort.. mais uniquement lorsque l'axe des X changera.		


###Animation 4 - pendule

Il s'agit de la classe `.anim4`
À mixer avec la classe .temps2sec et .temps3sec dans le meilleur des mondes… le 1sec n'étant pas idéal pour cette animation

L'animation crée une sensation de pendule.
Se balançant de gauche à droite sur l'axe des X, un notera également un changement de couleur ainsi que l'opacité.
L'opacité à 100% initialement, changement de couleur à la moitié de l'animation, puis de la moitié à la fin, disparait en opacité 0%.
Pour donner l'effet de pendule, le point de reptation se trouve au centre en haut de l'objet.
Pour accentuer l'impression de pendule, les objets ronds sont conseillés.


###Animation 5 - bouncingBall

Il s'agit de la classe `.anim5`
À mixer avec la classe .temps2sec dans le meilleur des mondes… le 1sec et le 3sec n'étant pas idéal pour cette animation

L’animation fait le mouvement d’une balle qui rebondit.
Elle se donne une force de poussé au début, ce qui l'a fait écrasé un peu ( en largeur ) et se propulse dans les airs ( sur l'axe des Y ) en étant écrasé ( en longueur ).
À la moitié de l'animation, il y a un effet de suspend de la balle qui redevient ronde durant un court instant pour finalement se déformer jusqu'à l'effet d'écrasement à la fin.
Une touche de couleur à été changé lors de l'ascension de la balle ( du rose au orange ) et à la descente de celle-ci ( orange au rose ).


##Ajouter l'animation à votre objet :

Pour utiliser les animations, vous devrez donc choisir une classe de temps de la catégorie 2 et la mixer avec une des animations de la catégorie 1.
À vous de choisir de prendre la classe infini si vous le souhaitez.

Par exemple, si vous voulez utiliser l'animation shakeShake sur un div, vous ajouter les classes à votre objet comme ceci :


`<div class="temps2sec anim2 infini"></div>`

> ou

`<div class="temps2sec anim2"></div>`

> si vous ne voulez pas que l'animation soit en continu...

Bien entendu, si vous désirez animer un simple div, vous devrez lui attribuer une seconde classe pour lui donner une dimension - width et height.

	Par exemple, créer une classe :

	.dimension {
		width: 50px;
		height: 50px;
	}


#À noter

Si vous désirez utiliser les animations sur du texte, et que vous voulez garder les couleurs de fond qui se trouve déjà dans l'animation, enlever le background- de backgound-color.
	
	exemple :

	background-color: #C06;

> vous écrirez alors :

	color: #C06;

Ainsi la couleur s'appliquera au texte et non au fond de votre objet.
Vous pouvez aussi enlever la couleur complètement si vous le souhaiter.

De plus, pour ne pas vous donner la sensation que la planète explose…
Vous devrez probablement donner une largeur (width) à votre texte si vous ne voulez pas que l'animation fasse la page au complet.
Après quoi, mettez le texte beau comme vous voulez, un text-align: center; si vous voulez qu'il soit beau dans le milieu de votre boîte texte.

Si toute fois l'envi vous prend de tout modifier le code afin de créer de nouvelle expérience avec mes animations, sachez que je ne suis aucunement responsable du résultat.
Alors si le tout est laid, vous ne me trouverai pas.
