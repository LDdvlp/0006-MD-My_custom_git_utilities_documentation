# 0006-MD-My_custom_git_utilities_documentation

## 1. Liste utilitaires

1. `gnp` - **Git New Project to GitHub** : créer un dépôt local et le pousser vers le dépôt distant du même nom, préalablement créé : `gnp repositoryName`.
*[0007-BASH-gnp-Git_New_Project_to_GitHub](https://github.com/LDdvlp/0007-BASH-gnp-Git_New_Project_to_GitHub)*
1. `gpp` - **Git Push Project to GitHub** : Pousser le **nouveau** dépôt local vers le dépôt distant du même nom, préalablement créé : `gpp repositoryName`.
*[0008-BASH-gpp-Git_Push_Project_to_GitHub](https://github.com/LDdvlp/0008-BASH-gpp-Git_Push_Project_to_GitHub)*
1. `gcp` - **Git Commit Project to GitHub** : Pousser le dépôt local **modifié** vers le dépôt distant du même nom, préalablement créé : `gpp repositoryName`. 
*[0009-BASH-gcp-Git_Commit_Project_to_GitHub](https://github.com/LDdvlp/0009-BASH-gcp-Git_Commit_Project_to_GitHub)*
1. `gvl` -  - **Git Version Latest** : affiche le dernier numéro de version de Git disponible sur le site : `gvl`.
*[0010-BASH-gvl-Dernier_numero_version_Git_du_website](https://github.com/LDdvlp/0010-BASH-gvl-Dernier_numero_version_Git_du_website)*
1. `gvu` -  - **Git Version Update** : compare le numéro de version actuel en local de Git et le dernier numéro de version disponible sur le site, puis propose une mise à jour si besoin : `gvu`.
*[0011-BASH-gvu-Versions_Git_actuel_et_a_venir_et_mise_a_jour](https://github.com/LDdvlp/0011-BASH-gvu-Versions_Git_actuel_et_a_venir_et_mise_a_jour)*

## 2. `gnp`, `gpp`, `gcp` en détail

|Commande|`gnp`|`gpp`|`gcp`|
|:---:|---|---|---|
|**Titre**|**Git New Project to GitHub**|**Git Add Project to GitHub**|**Git Add Commit Push Project to GitHub**|
|**Fichier**|`gnp.sh`|`gpp.sh`|`gcp.sh`|
|**Usage**<br />(Pas de guillemet !)|`gnp repositoryName`|`gpp repositoryName`|`gcp commitMessage`|
|**Instructions**|1. Création dossier<br />2. Aller dans dossier<br />3. Renseignement du README avec le nom du dossier en titre h1<br />4. Initialisation Git<br />5. Ajout à l'index<br />6. Commit<br />7. Création branche `main` et remplacement en force de la branche `master`<br />8. Connexion au dépôt<br />9. Envoi des données et mise à jour du dépôt|1. ***Le dossier existe***<br />2. ***On est dans le dossier***<br />3. Renseignement du README avec le nom du dossier en titre h1<br />4. Initialisation Git<br />5. Ajout à l'index<br />6. Commit<br />7. Création branche `main` et remplacement en force de la branche `master`<br />8. Connexion au dépôt<br />9. Envoi des données et mise à jour du dépôt|1. ***Le dossier existe***<br />2. ***On est dans le dossier***<br />3. ***Le README est déjà renseigné***<br />4. ***Git est déjà initialisé***<br />5. Ajout à l'index<br />6. Commit<br />7. **La  branche `main` est déjà créée et on est dessus**<br />8. ***Le dépôt est déjà connecté***<br />9. Envoi des données et mise à jour du dépôt|
|1|mkdir|-|-|
|2|cd|-|-|
|3|echo to `README.md`|echo to `README.md`|-|
|4|git init|git init|-|
|5|git add|git add|git add|
|6|git commit -m "v.1.0.0"|git commit -m "v.1.0.0"|git commit -m|
|7|git branch -M main|git branch -M main|-|
|8|git remote add origin|git remote add origin|-|
|9|git push -u origin main|git push -u origin main|git push -u origin main|

