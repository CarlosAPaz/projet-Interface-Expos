# projet-Interface-Expos
Projet : donner le design initial d'un site ouèbe pour les défunts Expos de Montréal respectant les directives suivantes


Vous devez donner le design initial d'un site ouèbe pour les défunts Expos de Montréal. Le site donnera une brève histoire de l'équipe et permettra d'observer sa composition pour chaque année de sa courte histoire: 1969-2004. Il sera également possible de consulter l'évolution du rendement de l'équipe au fil des ans. Le site que vous développez sera rédigé en français.

Le site devra être organisé comme le montre le plan que vous trouverez plus bas. Chaque bulle correspond à une "page" (ou une famille de pages, car la plupart seront générées dynamiquement) du site. Chaque page devra avoir une barre de navigation.

La page d'accueil (acceuil.html) décrit la mission du site et décrit un peu l'histoire de l'équipe. À partir de la page, il sera possible d'aller directement sur une des 4 pages du niveau inférieur. 

La page <<composition des équipes>> (composition.html) donnent un tableau de la composition de l'équipe pour une (ou des) année(s) de son histoire sélectionnée par le visiteur. Cette page donnera également accès à une page qui affiche son classement pour la saison sélectionnée. Une formation est donnée sous forme de tableau. 

La page <<classement des équipes>> (classement.html) permet de voir les statistiques de l'équipe pour une année sélectionnée par le visiteur. Les statistiques sont données sous forme de tableau donnant le classement des équipes de la ligue avec leurs statistiques.

La page <<évolution de l'équipe>> (evolution.html) permet de voir l'évolution de l'équipe au cours de son histoire sous forme graphique. Par exemple, la moyenne de l'équipe pour chaque année de son histoire.  Les tableaux seront  traités plus tard (avec javascript). 

La page <<les auteurs>> (auteurs.html) donnent les coordonnées des membres de l'équipe (Nom, Prenom, Matricule) qui a réalisé le site. Ceci nous permettra de vous identifier.

Vous devez définir des feuilles de style CSS (Vous pouvez choisir les noms de vos fichiers CSS) pour votre site. Les paramètres généraux ainsi qu'un ou des style(s) de tableaux. Vous devez également produire la page d'accueil ainsi que celle des auteurs.  Les pages <<composition>> et <<évolution>>  ne seront utilisés que pour montrer le(s) style(s) de tableaux sur des données sans signification. 


Le but de ce devoir est de réaliser l'interface usager  pour votre site ouèbe. Elle permettra à l'usager de  sélectionner ce qu'elle veut voir lorsqu'elle demande de l'information au sujet de la composition de l'équipe des Expos pour une année donnée. La même chose pour la page qui donne le classement des Expos pour une année. Attention, vos interfaces ne sont pas des formulaires, car les données ne sont pas transmises à un serveur comme telles. 

Les pages évolution de  l’équipe et auteurs ne seront pas modifiées pour ce devoir.

Pour aider la compréhension des attributs des tables Fielding, Batting, Pitching, etc., les acronymes pour les attributs  de la base de données peuvent être consultés ici:                  

 https://rdrr.io/cran/Lahman/man/.

Une autre liste des mêmes acronymes est disponible ici:   

https://www.baseball-almanac.com/stats4.shtml

Commençons par la page la plus simple à modifier.

1) La page du classement des équipes.

Sur cette page, vous permettez à l'usager de choisir une année et s'il veut le classement des deux ligues (nationale+américaine) où seulement la nationale. Les tableaux de classement pour les divisions est et ouest de la ligue nationale (et de l'Américaine si demandée) seront générés par du JavaScript au devoir #4. 

L'usager peut également demander de voir les champions de chacune des deux ligues (qui seront montrés par une marque dans le classement) et le champion de la série mondiale. 

Ces choix sont offerts par l'interface. Vous y ajoutez un bouton pour lancer le remplissage du tableau lorsque nous aurons vu comment au prochain devoir.

Cette interface est donc très très simple contrairement à la page de composition de l'équipe que nous décrivons maintenant.

2) La page de composition de l'équipe.

Sur cette page, l'usager devrait pouvoir sélectionner certains aspects de la composition de l'équipe pour une année donnée.

En premier lieu,  il doit y avoir un sélectionneur d'années pour une année de  la plage 1969— 2004, les années où les Expos étaient actifs.

L'usager peut maintenant sélectionner les attributs qu'elle veut voir dans les tableaux qui donneront la composition de l'équipe. En général, la composition de l'équipe devra indiquer:

a) Les joueurs qui ne sont pas des lanceurs (joueurs de champs),  

b) les lanceurs,

c) Le gérant (manager),

d) l’assistance,   

e) la masse salariale.

Les joueurs a), les lanceurs b)  seront présentés (au devoir #3) dans deux tableaux séparés. Chacun des tableaux doit avoir un identificateur id pour permettre à  JavaScript de produire le contenu des tableaux.

Le gérant c) n'est pas inclus dans les tableaux, mais est donné par une étiquette <label>. Chacune de ces 2 étiquettes (gérant+proprio)  devra avoir un id qui permettra à JavaScript d'y placer le nom du gérant. 

Vous placez les tableaux, le gérant, la masse salariale et l'assistance  de la façon que vous le désirez. L'assistance aux matchs à Montréal est également  donnée par une étiquette (i.e. <label>) avec un id unique pour les mêmes raisons. 

La même chose est demandée pour la masse salariale. Pour le moment, vous pouvez  placer des noms bidon pour le gérant, une valeur bidon pour l'assistance et un  montant bidon pour la masse salariale.

Les joueurs maintenant. Pour afficher le tableau a) des joueurs, l'usager doit être capable de spécifier les attributs qu'elle ou qu'il veut voir dans le tableau (ce qui correspondra aux colonnes du tableau affiché des joueurs). Vous devez fournir l'interface pour y arriver. Le tableau des joueurs contiendra toujours le nom de famille suivi du prénom des joueurs (par exemple, le prénom peut aussi être  abrégé si vous décidiez de permettre un affichage court à travers l'interface)  en première colonne.

Les autres attributs peuvent être choisis par l'usager. Voyons comment.

Le tableau contiendra les joueurs qui ont joué pour les expos (autrement que pour lancer) durant la saison sélectionnée avec leurs statistiques. Quelles statistiques seront montrées dans le tableau dépend des choix de l'usager. Les colonnes du tableau  sont séparées en deux parties, 1) les stats au bâton (offensive) et 2) celles en défensive. Les attributs sélectionnés pour l'offensive sont regroupés et ceux pour la défensive le sont également. L'usager peut sélectionner l'ensemble des attributs désirés parmi les suivants:

Offensive: BA%, SL%, OB%, SO%, SB%, AB, H, 1B, 2B, 3B, HR, BB,R, SB, CS,  où BA%=H/AB, SL%= (1B+ 2*2B+ 3*3B + 4*HR)/AB, OB% = (H+BB+HBP)/(AB+BB+HBP+SF), SO%=SO/AB et SB%=SB/(CS+SB).

Defensive: FP%, POS, A, E, salaire où FP% = A/(A+E).

L'usager devrait pouvoir sélectionner seulement l'offensive ou seulement la défensive ou un mélange des deux ou les deux en même temps. 

Vous devez également donner la possibilité à l'usager (en utilisant l'interface) de demander de trier les rangées tu tableau a) en fonction d'un  attribut parmi BA%, SL%, OB%, FP% ainsi que HR et salaire. 

L'important pour ce devoir est d'offrir ces choix de la meilleure façon par l'interface que vous mettez en place. Un tableau bidon, comme celui qui est déjà en place depuis le devoir #1, doit être positionné au  bon endroit. 

Le nombre de rangées du tableau n'est pas important. Placez-y environ 20 colonnes (ce qui correspond au nombre maximum d'attributs). 

Le tableau des lanceurs maintenant (tableau b)). Pour les lanceurs, les statistiques sont différentes. Celles que l'usager peut décider de voir sont  ERA, BAOpp, partant, G, GS, CG, W, L, SV, IPouts, SO, H, BB, salaire. 

L'attribut partant indique si un lanceur est un partant (i.e., GS>0) ou un releveur (G>0 mais GS=0). L'usager doit pouvoir voir les lanceurs triés dans le tableau en fonction d'un des attributs ERA, BAOpp, G, GS, CG, W, SO, H, BB ou salaire.

Ici également, vous devez ajouter un bouton (avec un id) (par tableau ou un pour les deux) pour lancer le remplissage des tableaux. 

 

Attention à la validation: https://validator.w3.org/#validate_by_upload !!!
