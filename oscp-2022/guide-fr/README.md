---
description: Préparation OSCP 2022
cover: >-
  https://parissecret.com/wp-content/uploads/2022/10/3715098.jpg-r_1920_1080-f_jpg-q_x-xxyxx.jpg
coverY: 23.494860499265783
---

# 🇫🇷 Guide (FR)

Voici l'approche que j'ai suivi pour réussir l'examen OSCP.

L'ensemble des conseils je vais vous présenter ici ne vous correspondront pas totalement.

Il ne s'agit pas de suivre ce guide à la lettre, prenez ce qui vous plait et oubliez le reste !&#x20;

## Auteur:

* [Twitter](https://twitter.com/sgtdede)
* [Github](https://github.com/sgtdede)
* [Linkedin](https://www.linkedin.com/in/andr%C3%A9-lenoir-9487a2152/)

7 ans d'expérience professionnelle dans la cybersécurité en offensif et défensif. Dont un nombre conséquent de pentests webs et pentests internes.&#x20;

Très peu de background en CTF et plateformes CTF (TryHackMe, HackTheLab, root-me, etc.)

## Palu Menfou:

* Insistez sur les labs, c'est de loin la ressource la plus rentable de la formation. Vous pourrez réussir l'examen en ignorant totalement les cours, mais pas en ignorant les labs.\

* La thématique de privilege escalation compte pour la moitié des points de l'examen (AD et standalones confondus).\
  Voici la meilleure introduction privesc pratique disponible sur internet: \
  [https://tryhackme.com/room/linuxprivesc](https://tryhackme.com/room/linuxprivesc)\
  [https://tryhackme.com/room/windows10privesc](https://tryhackme.com/room/windows10privesc)\
  Faites ces rooms et prenez des notes, elles vous feront gagner beaucoup de temps et d'assurance. La room Windows est un peu moins bien mais reste très intéressante.\

* Active Directory compte pour 40 points sur l'examen et valide les 2/3 de l'examen. Faites tous les exercices et labs du programme PEN-200 qui concernent AD, et entrainez vous aussi sur les box AD de TryHackMe, PG-PLAY et HackTheBox\

* Armageddon cheat sheet: [https://github.com/sgtdede/oscp/blob/main/armageddon.txt](https://github.com/sgtdede/oscp/blob/main/armageddon.txt)



## OSCP Exam:

Comme pour les labs PEN-200: vous devez trouver point d'entrée et prendre la main sur plusieurs machines (reconnaissance et exploitation) et passer root/système sur ces machines (privilege escalation).&#x20;

Il y a un total de 6 machines à pirater pendant l'examen.

* **1 environnement Active Directory (1 DC + 2 machines)** = 40 points
* **3 serveurs autonomes** = 20 points chacun (10 pwn + 10 privilege escalation)
* **Points Bonus** = 10 points
* **Points total possible** = 110 points (40 points AD + 60 points standalones (3x20) + 10 points bonus)
* **Points requis pour valider l'examen** = 70 points



## Recommandations:

### 1) Ressources disponibles: labs avant tout&#x20;

Voici les 4 ressources a votre disposition triées de la plus intéressante à la moins intéressante (de mon point de vue)

* Labs (Pen-200)
* PG-Play/PG-Practice/TryHackMe/HackTheBox (External labs)
  * [NetSecFocus lists (PG-Play, PG-Practice, HTB)](https://docs.google.com/spreadsheets/u/1/d/1dwSMIAPIam0PuRBkCiDI88pU3yzrqqHkDtBngUHNCw8/htmlview)\

* S1REN walkthroughs, IppSev walkthroughs, TCM courses,  writeups, etc. (Extern courses)
  * [S1REN walkthroughs](https://www.youtube.com/playlist?list=PLJrSyRNlZ2EeqkJa12Tu-Ezun9kXvHufN)
  * [IPPSec walkthroughs](https://www.youtube.com/watch?v=2DqdPcbYcy8\&list=PLidcsTyj9JXK-fnabFLVEvHinQ14Jy5tf\&ab\_channel=IppSec)
* Courses  + Exercices (Pen-200)

Je place les trois premières ressources loin devant la partie cours. et les walkthroughs à égalité en deuxième position avec les labs PG-PLAY/PG-PRACTICE. Les walkthroughs sont un très bon compléments aux labs et je vous conseille de travailler ces deux ressources en parallèle pendant la même période. En effet les walkthrough vont vous permettre d'augmenter votre capacité de resolution de labs. et les labs vont vous permettre d'être beaucoup plus proactifs pendant la lecture des walkthroughs.

Les principaux challenges que vous allez rencontrer pendant l'examen et la résolution des labs sont:

* trouvez des pistes d'attaques
* identifier rapidement les fausses pistes (rabbitholes)
* identifier les pistes d'attaques qui méritent d'être creusées

Seul l'expérience va vous permettre d'améliorer ces trois capacités. Plus vous allez faire de labs plus vous allez améliorer ces compétences, notamment l'identification des fausses pistes.&#x20;



### 2) Comment bien faire un lab

#### a- Eviter les indices/discord/forum

Perdez très rapidement l'habitude d'utiliser des indices et de vous référer aux forums et a Discord. Gardez bien en tête que si vous utilisez ces ressources en faisant un lab, vous ne vous améliorerez pas ou très peu les trois compétences: **identifier rapidement les fausses pistes (rabbitholes),** **trouver des pistes d'attaques** et **identifier les pistes d'attaques qui méritent d'être creusées** puisque les indices des forums/discord vont vous donner ces informations à votre place.

Cela étant dis vous pouvez vous y référer beaucoup au début, lors de vos premiers labs, surtout si vous êtes débutant.

Par la suite, fixez vous des règles:

* Ne vous référez jamais a discord/forum si vous n'avez pas passé un temps significatif sur les étapes de reconnaissance. Forcez vous a exploiter toutes les pistes avant d'y songer.
* Vous pouvez sans problème vous référer au discord/forum après avoir résolu une box, pour vérifier si il y avait une alternative meilleure/plus simple. Ou si vous estimez que vous n'auriez pas du passer en utilisant le chemin d'exploitation que vous avez pris. &#x20;

Il existe un seule exception: si vous devez valider vos 30 labs pour avoir 10 points bonus pour l'examen et que vous êtes trop juste en temps. Alors dans ce cas et dans ce cas uniquement, faites au plus efficace possible (mais gardez bien en tête que vous allez perdre tous les autres bénéfices liées à la résolution des labs).

Certains labs sont mal construits ou obsolètes, fixez vous une limite de temps et ne perdez pas plusieurs jours sur ce genre de labs. Si vous estimez que vous avez fait une recherche complète et que vous êtes à court d'idée, alors référez vous a discord/forum.

#### b- Prenez des notes

Prenez des notes tout au long de votre exploitation (screenshots + écrits + preuves). Inspirez vous de la méthode de S1REN qui est simple et efficace (cf. [S1REN walkthroughs](https://www.youtube.com/playlist?list=PLJrSyRNlZ2EeqkJa12Tu-Ezun9kXvHufN)).  Cette méthodologie et la prise de notes régulière vous apporteront beaucoup sur la durée.

Pendant votre exploitation ou à la fin d'une box, alimentez une Cheat Sheet dédiée pour cette box avec les commandes clés qui vous on permis d'exploiter la box (reconnaissance, exploitation et privilege escalation)

Voici mon templace CherryTree pour une box : [https://github.com/sgtdede/oscp/blob/main/target.ctb](https://github.com/sgtdede/oscp/blob/main/target.ctb)

![](<../../.gitbook/assets/image (2).png>)

Je note l'ensemble des étapes de reconnaissances dans l'onglet **Report.**



**Dernier conseil:** ne chargez pas trop la mule: si vous êtes dans un mauvais état d'esprit (saturé, impatient, pas envie de chercher la vuln) alors c'est peut etre mieux de reprendre le lab une autre fois, ou de se changer les idées avant (prendre l'air, sport, etc.). Dans cet état là vous n'arriverez probablement à rien de toute façon et vous en ressortirez encore plus frustré.



### 3) Comment bien faire un walkthrough

Ne passer pas en pilotage automatique ! Les walkthrough youtube et writeups sont d'excellentes ressources mais si vous les écoutez à moitié ils ne servent à rien et vous les aurez oublié la semaine suivante.&#x20;

* Alimentez vos notes et votre cheatsheet pendant la lecture du walkthrough: toutes les commandes que vous ne connaissez pas et qui vous semblent intéressantes à ajouter à votre arsenal
* Mettez la vidéo en pause régulièrement avant la résolution et mettez vous complétement à la place de l'attaquant: Que feriez vous à la place de S1REN/IPPSec? Quelle commande lanceriez vous? quel service scanneriez vous ? Quels pistes d'attaques exploreriez vous ?\
  Lorsque vous êtes prêts reprenez la vidéo et comparez, si vous aviez trouvé: bravo ! essayez de repérer les différences d'outils ou options utilisés dans la walkthrough pour éventuellement enrichir votre arsenal ou découvrir une autre méthode d'exploitation.\
  Sinon, ça veut dire que vous êtes passé à coté de quelque chose, notez le et prévoyez de travailler à nouveau dessus.\
  Faites ce travail a chaque étape de l'exploitation, après le scan nmap, après avoir découvert un service vulnérable, avant l'escalade de privilège, etc.
* Lors de la résolution de vos labs, essayez de prendre conscience ou noter vos faiblesses. Essayez d'y repenser lorsque vous regardez un walkthrough et de repérer comment font S1REN/IPPSec/etc. face à ces mêmes problèmes, cela vous permettra surement de découvrir de nouveaux concepts/outils et d'améliorer ces faiblesses.

Si vous faites correctement ces étapes vous tirerez le maximum des videos walkthrough et writeups et dans ce cas il s'agit d'une ressource hyper efficace !



### 4) Active Directory

Active Directory fait son apparition depuis 2022 dans l'examen et compte pour 40 points. AD est inévitable le jour l'examen, il compte pour 2/3 des points nécessaires pour obtenir la certif à lui tout seul. Sachez que l'exploitation des environnements AD n'est pas très variée et globalement vous n'aurez pas beaucoup de surprises si vous maîtrisez les concepts à connaître pour l'exploitation AD. Le seul élément vraiment changeant sera le point d'entrée.&#x20;

La difficulté pour s'entrainer sur AD est le manque de ressources: le cours PEN-200 AD est mauvais, les exercices sont par contre très bons et les labs aussi, mais il y en a très peu. Donc il faut les faire tous: tous les exercices et tous les labs. N'hésitez pas a les refaires plusieurs fois pour être à l'aise sur l'exploitation AD (ici on laisse de côté l'initial foothold), essayer de matriser plusieurs outils/méthodes (2 ou 3) différents pour chaque étapes d'exploitation AD, pour les déplacements latéraux et pour le pivoting.

**Ressources supplémentaires:**

* [https://tryhackme.com/room/wreath](https://tryhackme.com/room/wreath)
* [https://tryhackme.com/room/adenumeration](https://tryhackme.com/room/adenumeration)
* [https://tryhackme.com/room/vulnnetroasted](https://tryhackme.com/room/vulnnetroasted)
* [https://tryhackme.com/room/postexploit](https://tryhackme.com/room/postexploit)
* [https://tryhackme.com/jr/lateralmovementandpivoting](https://tryhackme.com/jr/lateralmovementandpivoting)
* [https://tryhackme.com/room/enterprise](https://tryhackme.com/room/enterprise) (plus compliqué que l'OSCP)

****

### 5) Privilege Escalation

La thématique de privilege escalation compte pour la moitié des points totaux de l'examen (AD et standalones confondues):

Faites les deux rooms TryHackMe suivantes, elles vous feront gagner beaucoup de temps et d'assurance:\
[https://tryhackme.com/room/linuxprivesc](https://tryhackme.com/room/linuxprivesc)\
[https://tryhackme.com/room/windows10privesc](https://tryhackme.com/room/windows10privesc)

#### a- Scripts d'énumération privesc

Les scripts/binaires d'énumération automatique sont très efficaces et je vous recommande de les utiliser.&#x20;

**Windows:** winpeas, powerup, sharpup

**Linux:** LinEnum.sh, linpeas.sh

Pour l'OSCP sur linux, j'utilisais autant LinEnum que linpeas. Sur Windows, j'utilisais principalement WinPeas par habitude mais je pense que powerup/sharpup sont plus rentables dans un premier temps car WinPeas a tendance a remonter beaucoup trop d'information et de bruit. Je vous conseille quoiqu'il arrive d'en avoir au moins deux sous la main pour chaque OS.&#x20;

**Attention:** comme pour autorecon (cf. [reconnaissance](./#6-reconnaissance)), ce sont des outils à double tranchant:\
ils vont avoir tendance à vous faire passer en pilotage automatique, ce que vous devez absolument éviter. Et ils vont ressortir tellement d'informations que vous allez parfois passer à coté d'une privilege escalation très simple et partir sur une fausse piste. Enfin, parfois les privileges escalations ne seront pas trouvées par ces scripts.

C'est pourquoi je vous recommande fortement pendant votre entrainement sur les labs de faire quelques énumérations manuelles, pour comprendre et vous familiariser avec les principales méthodes de privilege escalation sur Linux et Windows. Les deux room TryHackMe vont aussi énormément vous aider pour ça !

#### b- Enumération manuelle

Si vous regardez les walkthrough de S1REN, elle fait systématiquement les privilege escalation en énumération manuelle et n'utilise jamais les scripts. Regarder quelques uns de ses walkthroughs est aussi une bonne méthode pour apprendre à rechercher les privilege escalations.

Voici quelques ressources que vous pouvez utiliser pour les énumérations manuelles.

* [https://book.hacktricks.xyz/windows-hardening/windows-local-privilege-escalation](https://book.hacktricks.xyz/windows-hardening/windows-local-privilege-escalation)
* [https://sirensecurity.io/blog/linux-privilege-escalation-resources/](https://sirensecurity.io/blog/linux-privilege-escalation-resources/)
* [https://sirensecurity.io/blog/windows-privilege-escalation-resources/](https://sirensecurity.io/blog/windows-privilege-escalation-resources/)



### 6) Reconnaissance

* **Utilisez** [**Autorecon** ](https://github.com/Tib3rius/AutoRecon)**(ou équivalent) en scanner secondaire**
* **Faites toujours passez vos scans manuels pour ne pas passer en pilotage automatique et ne pas "subir" les résultats**

L'étape la plus important pour chaque box des labs et de l'exam. Passer du temps sur cette étape vous permettra d'identifier les pistes d'attaques et d'identifier plus rapidement les fausses pistes (rabbit holes). Plus vous allez faire de labs et plus vous allez vous améliorer.

Prenez l'habitude d'essayer plusieurs outils différents sur toutes les étapes de l'exploitation mais particulièrement pour la reconnaissance. En effet dans certains cas certains outils ne seront pas compatibles ou moins complets face à certain OS, services, versions et vous feront peut passé à côté du point d'entrée.

Ne vous éparpillez pas trop néanmoins, pas besoin de maîtriser parfaitement plusieurs outils, je vous conseille de maitriser et être confortable avec un outil pour chaque type de reconnaissance,  mais de savoir en utiliser d'autres  en complétements. Par exemple, mes outil référence étaient: nmap pour les scans de ports, tunnel ssh/chisel pour le pivoting, ffuf pour le fuzzing web, impacket pour la post exploitation windows/Active Directory, etc.

Autorecon est un outil très puissant de ce point de vue là pour la phase de reconnaissance, car il scanne chaque service avec plusieurs outils différents. Néanmoins c'est un outil à double-tranchant qui peut se retourner contre vous:&#x20;

* ne passez pas en pilotage automatique : autorecon peut vous faire devenir très passif et vous pouvez tomber dans le piège de penser qu'il fait déjà tout pour vous et mieux que si vous le faisiez vous-même. Ce n'est pas le cas et cela vous met dans un posture que vous voulez éviter à tout prix !&#x20;
* il va retourner énormément d'informations, parfois trop, et peu vous faire creuser des fausses pistes que vous n'auriez jamais exploré avec vos propres scans.

Gardez votre intuition et fabriquez vous toujours un plan d'attaque. Je vous recommande fortement d'utiliser Autorecon, mais en scanner **secondaire**. Quand vous attaquez une box (lab ou exam) laissez tourner autorecon en fond, mais utilisez vos scanner "manuels" en premier.&#x20;

Référez-vous à Autorecon que pour valider/appuyer ce que vous avez déjà trouvé avec vos scan, si vous avez de fortes suspicions sur un service après vos premiers scans, ou dans le cas ou vous n'avez plus aucune piste !



### 7) Prise de notes CherryTree, OneNote, Obsidian, Joplin&#x20;

* **Familiarisez vous avec un outil de prise de note qui vous sera utile tout au long de la formation, pour les labs, pour l'exam et aussi pour vos futurs pentests.**

Choisissez l'outil qui vous convient le mieux, personnellement j'en ai testé beaucoup pendant ma formation et j'ai fini par choisir CherryTree. C'est le plus moche mais c'est celui me convenait le mieux. Il est simple a apprendre, rapide, avec des raccourcis pratiques et la meilleure structure de tous les outils de prises de notes que j'ai pu tester.

Voici mon template que j'ai utilisé pour les labs et pour les machines de l'exam OSCP: [https://github.com/sgtdede/oscp/blob/main/target.ctb](https://github.com/sgtdede/oscp/blob/main/target.ctb)

![](<../../.gitbook/assets/image (2).png>)

Je note l'ensemble des étapes de reconnaissances dans l'onglet **Report** (structure inspirée très fortement de S1REN).

Je vous recommande de regarder quelques walkthroughs de S1REN et de vous en inspirer pour la prise de notes et la méthodologie.



### 8) Cheat Sheet

* **Faites vos propres cheat sheet, gardez les cheat sheet externes en références pour ne pas passer en pilotage automatique**
* **A la fin de votre préparation, compilez l'ensemble de vos cheat sheet pour vous préparer une cheat sheet ultime (armageddon) dédiée à l'examen qui sera beaucoup plus légère**&#x20;

Tout au long de votre formation, maintenez à jour une ou plusieurs CheatSheet. Personnellement j'ai maintenu plusieurs CheatSheet générales sur toutes les thématiques de l'OSCP. Je les ai enrichies au fur et à mesure ces cours, labs et walkthroughs. J'ai noté toutes les commandes qui me semblaient importantes ou qui pouvaient m'être utiles un jour.

Finalement ces Cheat Sheet se sont révélées un peu trop fournies par rapport aux commandes/outils dont j'avais besoin 80% du temps. Je mettais trop de temps à retrouver les informations qu'il me fallait.&#x20;

Donc j'ai fais une Cheat Sheet beaucoup plus compacte spécialement pour l'examen. Et qui contenait les uniquement les commandes que j'utilises 80% du temps. (en backup j'avais toujours mes autres cheat sheet beaucoup plus riches pour quand je tombe sur les 20% restants).

#### Armageddon Cheat Sheet (CheatSheet dédiée pour l'examen)

Ici retirez tous ce qui n'a pas de rapport avec l'OSCP et l'examen, le but c'est de ce concentrer sur l'examen spécifiquement, pas sur tout ce que vous avez appris pendant la formation, donc:

* Reconnaissance/exploitation
* Active Directory
* Privilege Escalation
* Toutes les commandes et outils que vous utilisez fréquemment dans vos labs, toutes vos commandes préférées

A titre d'exemple, voici ma Cheat Sheet armaggedon que j'ai préparé pour l'exam: [https://github.com/sgtdede/oscp/blob/main/armageddon.txt](https://github.com/sgtdede/oscp/blob/main/armageddon.txt)

Encore une fois j'insiste sur le fait qu'elle est efficace parce que c'est la mienne, elle ne sera probablement pas aussi intéressante pour vous. Faites vous votre propre liste Armageddon, vous ne le regretterez pas.

#### Cheat Sheet références:

* [https://github.com/swisskyrepo/PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)
* [https://www.thehacker.recipes/](https://www.thehacker.recipes/)
* [https://book.hacktricks.xyz/welcome/readme](https://book.hacktricks.xyz/welcome/readme)
* [https://www.ired.team/](https://www.ired.team/)
* [https://www.hackingarticles.in/](https://www.hackingarticles.in/)



### 9) Points bonus (10 points)

Il est possible d'avoir 10 points bonus sur la note final en remplissant les objectifs suivants:

* Compléter tous les exercices de la partie cours de PEN-200
* Rooter 30 machines sur les labs PEN-200

Si vous suivez mon guide vous allez remplir le deuxième objectif naturellement. Je vous recommande fortement de faire le plus de labs possibles avant l'examen, et donc au minimum 30.

Les exercices sont selon moi très bien mais le problème est que pour valider l'ensemble des exercices vous allez devoir passer par le cours de la PEN-200 qui lui n'est vraiment pas terrible.&#x20;

Si vous avez un an de formation, alors il n'y a pas de question: faites la partie cours et l'ensemble des exercices: 10 points cela peut etre la différence entre une réussite ou un échec à l'examen final.

Si vous avez un mois de formation vous n'aurez probablement pas le temps de faire correctement les labs et les exercices je vous recommande d'investir tout votre temps en labs/walkthroughs.

Si vous avez 3 mois d'accès la décision n'est pas simple: en moyenne le cours/exercice peut vous prendre près d'un mois, et en dehors des 10 points ne vous apportera pas énormément. Personnellement j'ai travaillé 2 mois sur la plateforme PEN-200, j'ai fais un mois sur les cours et exercices et 1 mois sur les labs. Avant l'examen et après coup j'ai eu l'impression que j'aurais mieux fait de faire 2 mois de labs et sauter les exercices. Néanmoins ce n'est pas un choix facile a faire car les 10 points bonus peuvent changer la donne sur l'examen final.



### 10) Planning

* 1 mois d'accès aux labs
* 3 mois d'accès aux labs
* 12 mois d'accès aux labs

Pour les formules à 1 ou 3 mois, n'hésistez pas à ajouter dans votre planning 1 ou plusieurs mois d'accès à PG-PLAY/PG-PRACTICE (éventuellement HackTheBox) si vous ne vous sentez pas confortable a la fin de vos labs pour continuer l'entrainement avant l'exam.

Mais il faut battre le fer tant qu'il est chaud et je pense qu'il vaut mieux passer l'exam directement après un mois d'entrainement intensif en étant affuté, meme si vous n'estimez pas être prêt à 100%, plutôt que de décaler l'examen a un mois supplémentaire si vous savez que vous allez lever le pied sur ce mois supplémentaire. &#x20;

Vous trouverez mes recommandations spécifiques pour chaque types de profil (débutant, ctf player, pentester).

Selon votre niveau/expérience il est tout à fait possible de réussir l'OSCP avec un accès d'un mois (voire sans aucun entrainement sur PEN-200).



### 11) Examen

Prévoyez un peu de temps pour prendre en compte les conditions de l'examen:

* [https://help.offensive-security.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide](https://help.offensive-security.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide)
* [https://help.offensive-security.com/hc/en-us/articles/360050299352-Proctoring-Tool-Student-Manual](https://help.offensive-security.com/hc/en-us/articles/360050299352-Proctoring-Tool-Student-Manual)

N'hésitez pas à revert la machine que vous attaquez au moindre doute.

Essayez de prévoir basiquement un plan initial sans pour autant vous bloquer complétement: personnellement j'ai choisi de commencer par l'environnement AD, qui me semble le moins stressant car je me disais que pour valider l'examen il fallait valider les 40 points de l'AD absolument.

Prévoyez à l'avance des repas, boissons, cafés etc. pour vous faire gagner du temps et relâcher la pression si jamais vous vous retrouver en situation compliquée et que cela ce joue sur les dernières heures: en bref, mettez toutes les chances de votre côté.

Respirez et détendez vous, ne changez pas vos habitudes et utiliser vos méthodes classiques. Comme si vous étiez en train d'exploiter des box du lab PEN-200.&#x20;

Ce n'est pas grave de passer beaucoup de temps sur une box, vous avez besoin de 70 points uniquement, même si vous débloquez les premières machines très tard, l'examen est toujours jouable.

Si vous échouez à l'examen, ce n'est pas la fin du monde, vous reviendrez plus fort la prochaine fois.



### 12) (optionnel) Rapport

J'ai utilisé Word et le [template ](https://www.offensive-security.com/pwk-online/OSCP-Exam-Report.docx)fourni par offensive security pour la simple et bonne raison que je n'avais pas envie de passer du temps pour apprendre un nouvel outil qui n'est pas nécessaire et qui ne m'apportera rien pour l'OSCP.

Faites selon vos préférences, je vous conseille de prendre l'outil avec lequel vous êtes déjà le plus familier, il y a déjà tellement de travail et d'outils à apprendre pour bien préparer l'OSCP qu'il n'est pas nécessaire de s'en rajouter en plus inutilement... A la place profitez en pour prendre l'air, faire du sport, passer du temps en famille et vous changer les idées :)

&#x20;

### 13) (optionnel) Editeur de texte vim/nano

L'éditeur de texte c'est une autre histoire et de mon point de vue il vous sera quasi indispensable d'être confortable sur vim ou nano. Les deux éditeur sont puissants et présent sur une majorité de systèmes Linux. A choisir, petite préférence pour vim car c'est l'éditeur que vous retrouverez tout le temps sur les Linux/UNIX que vous exploiterez (dans PEN-200 et dans votre vie de pentester).

C'est un outil très puissant, qui vous fera gagner énormément de temps sur un grand nombre de tâches de hacking et d'administration au quotidien.&#x20;

{% embed url="https://danielmiessler.com/study/vim/" %}

### 14) (optionnel) Multiplexeur de terminal tmux/screen/terminator

De la meme façon, je vous recommande de vous familiariser avec un multiplexeur de terminal. C'est aussi un outil très puissant qui vous facilitera la vie au quotidien et vous fera gagner beaucoup de temps.

Personnellement j'utilise terminator car c'est celui que je connais déjà le mieux. C'est le plus facile à aborder mais il est moins puissant que les deux autres. A choisir, je vous recommande d'utiliser tmux, qui est aussi présent nativement sur un certain nombre de linux/unix et très adaptés pour le pentest.

{% embed url="https://www.youtube.com/watch?v=Lqehvpe_djs&ab_channel=IppSec" %}

## Mon parcours OSCP:&#x20;

[mon parcours](mon-parcours.md)



