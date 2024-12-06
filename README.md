# Navigation_script

Réalisation de mon script de navigation pour sélectionner un élément aléatoire des offres spéciales proposé par le site easyTravel.

##Réalisation:
- Pour ce faire j'ai dû récupérer la liste des id et en choisir un de manière aléatoire. Il est possible de voir la variable contenant l'élément séléctionné en suivant ce chemin:
  
  ``SC00_Navigation  =>  TR00_Accueil  =>  /easytravel/rest/journeys/special-offers  =>  /easytravel/rest/journeys/special-offers``
  
  Il faut ensuite visiter la catégorie **"Avancé..."** pour trouver notre variable **"EX_Rand_SelectItemID"**

  
- Suite à cela il faudra suivre ce chemin:
  
  ``SC00_Navigation  =>  TR01_Item  =>  /easytravel/rest/journeys/-{EX_RandSelectedItemID}``
  
  On pourra voir que j'ai édité l'url pour récupérer de manière dynamique l'id de l'élément envoyé. Dans la partie URL
  
  ``https://easytravel.gamman.fr:443/easytravel/rest/journeys/-${EX_RandSelectemItemID}``
