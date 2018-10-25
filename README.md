# DISCONTINUED

# solus-wine-staging-repository
Repository for solus which includes wine package built with staging patches.

# Enable repository
Add the repository by running:
```
sudo eopkg ar SolusWineStaging http://raw.github.com/community-repositories-for-solus/solus-wine-staging-repo/stable/eopkg-index.xml.xz
```
Then put the Solus official repository below this repository by removing it and adding it agaain:
```
sudo eopkg rr Solus
sudo eopkg ar Solus https://mirrors.rit.edu/solus/packages/shannon/eopkg-index.xml.xz
```
Then run `eopkg lr` to make sure that the repositories are in the correct order (SolusWineStaging must have higher position). Finally run `sudo eopkg ur -f` in order to refresh th repositories and `sudo eopkg up` in order to update wine.

# Revert Changes
In order to revert the changes you need to remove my repository and then reinstall wine package from the official repositories. run
```
sudo eopkg rr SolusWineStaging
sudo eopkg it --reinstall wine wine-32bit
```
