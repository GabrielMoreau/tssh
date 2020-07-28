# Tssh - ClusterSSH en mode terminal (tmux)

[tssh](https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh) est un script Bash permettant de lancer N terminaux sur N machines différentes via SSH.
Contrairement à ClusterSSH qui est en mode graphique,
```tssh``` utilise ```tmux``` pour multiplexer les sessions SSH dans le même terminal.

Un moyen simple d'utiliser la dernière version de [tssh]([https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh/-/raw/master/tssh?inline=false)
sans récupérer tout le repository est de faire :
```bash
wget https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh/-/raw/master/tssh?inline=false -O tssh
chmod u+x ./tssh
```

L'utilisation de ```tssh``` est dans le [manuel](https://legi.gricad-pages.univ-grenoble-alpes.fr/soft/trokata/tssh/).
```bash
man tssh
```

## Dépendances

Sous Debian, ```tssh``` nécessite les paquetages suivants :
```bash
apt-get install tmux wamerican # or wfrench
```
```wamerican``` (ou equivalent) est nécessaire pour le fichier ```/usr/share/dict/words```.
Un mot est pioché aléatoirement pour chaque session ```tmux```.


## Repository

### Source

L'ensemble du code est sous **licence libre**.
Le script en ```bash``` est sous GPL version 2 ou plus récente (http://www.gnu.org/licenses/gpl.html).

Tous les sources sont disponibles sur la forge du campus de Grenoble :
https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh

Les sources sont gérés via Git (GitLab).
Il est très facile de rester synchronisé par rapport à ces sources.

 * la récupération initiale

```bash
git clone ttps://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh
```
 * les mises à jour par la suite
```bash
git pull
```

### Téléchargement / Download

Des paquets Debian à jour sur https://legi.gricad-pages.univ-grenoble-alpes.fr/soft/trokata/tssh/download.

À noter que les paquets Debian sont très simples et ne vérifient certainement pas toutes les règles de la charte Debian.
Il sont cependant fonctionnels et en production au LEGI.

Si une personne sait comment faire un ```rpm```
et nous donne la recette, nous l’appliquerons.

### Patch

Il est possible d'avoir un accès en écriture à la forge
sur demande motivée à [Gabriel Moreau](mailto:Gabriel.Moreau A_ legi.grenoble-inp.fr).
Pour des questions de temps d'administration et de sécurité,
la forge n'est pas accessible en écriture sans autorisation.
Pour des questions de décentralisation du web, d'autonomie
et de non allégeance au centralisme ambiant (et nord américain),
nous utilisons notre propre forge...

Vous pouvez proposer un patch par courriel d'un fichier particulier via la commande ```diff```.
```bash
diff -u tssh.org tssh.new > tssh.patch
```
On applique le patch (après l'avoir lu et relu) via la commande
```bash
patch -p0 < tssh.patch
```
