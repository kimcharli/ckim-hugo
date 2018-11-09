```bash
hugo new project ckim-hugo
cd ckim-hugo
git init
git remote add origin git@github.com:kimcharli/ckim-hugo.git
git add -A
git commit -m "initail commit"
git push origin master

```


once
https://gohugo.io/hosting-and-deployment/hosting-on-github/
```bash
git remote add upstream git@github.com:kimcharli/ckim-hugo.git
echo "public" >> .gitignore

git checkout --orphan gh-pages
git reset --hard
git commit --allow-empty -m "Initializing gh-pages branch"
git push upstream gh-pages
git checkout master

```
