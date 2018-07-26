## How to create a new GitHub repository from command line
### and add code in an existing directory

Create a new **GitHub** repository via the command line using the **Github API**.

```
curl -u 'vadim-ivlev' https://api.github.com/user/repos -d '{"name":"create-new-github-repo"}'
```


Create a new repository on the command line
```
git init
git add -A .
git commit -m "."
git remote add origin git@github.com:vadim-ivlev/create-new-github-repo.git
git push -u origin master
```

If you have an existing local repository, you can push it to GitHub from the command line
```
git remote add origin git@github.com:USER/REPO.git
git push -u origin master
```

Dont forget to replace USER with your username and REPO with your repository name.

[Article on stackoverflow](https://stackoverflow.com/questions/2423777/is-it-possible-to-create-a-remote-repo-on-github-from-the-cli-without-opening-br)