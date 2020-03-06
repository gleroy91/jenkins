## Description et choix de l'outil de CI/CD 

J'ai commencé par forker le projet jenkins sur mon github. 

J'ai ensuite décidé d'utiliser l'outil de CI/CD integré directement à github, à savoir github Actions, pour plus de simplicité. 

## Explications sur le workflow

Le workflow que j'ai créé se nomme CI_Java. Chaque étape est commentée dans le fichier yaml correpondant.  

Les consignes du TP stipulent d'implémenter 4 differentes phases: build, tester avec java 8, tester avec java 14, deployer. 
Chacune de ces phases se traduit par un job dans github Actions. Les jobs s'effectuant par defaut en parallèle, j'ai conditionné l'execution des phases de test au sucess de l'etape de build, puis celle de la pahse de deploiement à la resussite des tests, au moyen du mot-clef "need". 

## Pourquoi ça ne marche pas ?

La phase de build se déroule sans accroc mais la generation du maven site ne fonctionne pas pour une raison que je n'arrive pas à identifier proprement (voir l'historique des lancements du workflow pour plus de détails).


