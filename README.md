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
if the last command gives the error: 
```
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.
```
then you need to add your public RSA key to the GitHub. The key is located in ~/.ssh/id_rsa.pub file. 
If you don't have one generate it with the following command:
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com".
```
Copy and paste the content of id_rsa.pub into your **Github profile -> Settings -> SSH and GPG Keys -> Add new SSH key**

More information is here: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/



To add an existing local repository to GitHub, push it from the command line
```
git remote add origin git@github.com:USER/REPO.git
git push -u origin master
```

Dont forget to replace USER with your username and REPO with your repository name.

[Article on stackoverflow](https://stackoverflow.com/questions/2423777/is-it-possible-to-create-a-remote-repo-on-github-from-the-cli-without-opening-br)