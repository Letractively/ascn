# Créer un jeu #

## Installation ##


**Ajouter une entrée dans la base de données :
:title : Nom du jeu qui sera affiché
:name : Nom code du jeu. Pas d'espace ni majuscules
:description : Sera affichée sous le titre**

**Créer un dossier dans www/games/JEUNAME**

### Fichiers ###

**index.php :**<pre>
<?php<br>
require_once '../../../config.php';<br>
env()->initJeu('JEUNAME');<br>
jeu()->run();<br>
</pre>

**JEUNAME.css :
CSS du jeu, sera inclue automatiquement**

**JEUNAME.js :
Script du jeu, sera inclu automatiquement**

**JEUNAME.tpl :
Template Smarty du jeu**

**JEUNAME.php
Classe PHP du jeu :**<pre>
<?php<br>
<br>
class TicTacToe extends Jeu {<br>
<br>
public function process() {<br>
// Controlleur du template smarty<br>
}<br>
<br>
public function getInitialData() {<br>
// Retourne un object contenant les données<br>
// initiale de la partie<br>
}<br>
}<br>
<br>
</pre>
