# Tssh - ClusterSSH in terminal mode (tmux)

[tssh](https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh)
is a Bash script allowing to launch N terminals on N different machines via SSH.
Unlike ClusterSSH which is in graphical mode,
```tssh``` uses ```tmux``` to multiplex SSH sessions in the same terminal.

More on [ClusterSSH](https://github.com/duncs/clusterssh).

## Usage

A simple way to use the latest version of
[tssh]([https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh/-/raw/master/tssh?inline=false)
without getting the whole repository is to do:
```bash
wget https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh/-/raw/master/tssh?inline=false -O tssh
chmod u+x ./tssh
```

The use of ```tssh``` is explained in the online
[manual](https://legi.gricad-pages.univ-grenoble-alpes.fr/soft/trokata/tssh/).
```bash
man tssh
```

### Dependencies

Under Debian, ```tssh``` requires the following packages:
```bash
apt install tmux wamerican # or wfrench
```
The ```wamerican``` package (or equivalent) is needed for the ```/usr/share/dict/words``` file.
A word is randomly selected for each ```tmux``` session.

### Download / Ready-made package

Up-to-date Debian packages can be found at https://legi.gricad-pages.univ-grenoble-alpes.fr/soft/trokata/tssh/download.

Please note that the Debian packages are very simple
and certainly do not check all the Debian Policy rules and quality.
They are however functional and in production at LEGI.

If someone knows how to make a package in ```rpm``` format
and gives us the recipe, we will apply it.

## Repository / Contribute

### Source

The whole code is under **free license**.
The script in ```bash``` is under GPL version 2 or more recent (http://www.gnu.org/licenses/gpl.html).
All the source code is available on the forge of the Grenoble campus:
https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh
The sources are managed via Git (GitLab).
It is very easy to stay synchronized with these sources.

Note: The master Git repository in on the [GRICAD Gitlab](https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh).
Other Git repository are mirror or fork.

 * The initial recovery
```bash
git clone https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/tssh
```
 * The updates afterwards
```bash
git pull
```
 * Contribute.
   It is possible to contribute by proposing pull requests,
   merge requests or simply old fashioned patches.

### Patch

It is possible to have a writing access to the project on the forge
on motivated request to [Gabriel Moreau](mailto:Gabriel.Moreau__AT__univ-grenoble-alpes.fr).
For questions of administration time and security,
the project is not directly accessible in writing without authorization.
For questions of decentralization of the web, of autonomy
and non-allegiance to the ambient (and North American) centralism,
we use the forge of the university campus of Grenoble...

You can propose a patch by email of a particular file via the ```diff``` command:
```bash
diff -u tssh.org tssh.new > tssh.patch
```
The patch is applied (after reading and rereading it) via the command:
```bash
patch -p0 < tssh.patch
```
