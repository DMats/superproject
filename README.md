# superproject setup

1. Setup SSH (required because submodule URL is SSH)
2. Clone repo using SSH
```console
git clone git@github.com:DMats/superproject.git
```
3. Initialize and update submodule.  This command resets the submodules to the
   commit stored in `.gitmodules`.
```console
# `--init` flag only required once in freshly cloned repo
git submodule update --init
```

# Change submodule commit
To change the submodule commit:

1. navigate into the submodule
```console
cd submodule/
```
2. checkout the desired commit
```console
git pull
```
3. navigate back to the superproject repo root
```console
cd ../
```
4. add/commit the new commit hash stored inside `.gitmodule`
```console
git add .gitmodule
git commit
```

# superproject creation log
These are the steps used to create the superproject.

1. Create repo in Github
2. Console commands:
```console
echo "# superproject" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:DMats/superproject.git
git push -u origin main
```
3. Add submodule:
```console
git submodule add git@github.com:DMats/submodule.git
```
4. Initialize and update submodules:
```console
# `--init` flag only required once in freshly cloned repo
git submodule update --init
```
