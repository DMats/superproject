# superproject setup steps

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

