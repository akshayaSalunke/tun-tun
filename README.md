# tun-tun

## Steps

```
➜  git init tun-tun

Initialized empty Git repository in /Users/akshayss/github/tun-tun/.git/
```

```
➜  cd tun-tun
```

```
➜  ls
```

```
➜  vim tun_tun.py
```

```
➜  cat tun_tun.py
print("tun tun likes chiwda, chakli, bakerwadi, kaju katli, rasmalai, gulab jamun, chai!")
```

```
➜  git add tun_tun.py
```

```
➜  git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   tun_tun.py
```

```
➜  git commit -m "list of indian food items that tun tun loves"
[master (root-commit) 8891e08] list of indian food items that tun tun loves
 1 file changed, 1 insertion(+)
 create mode 100644 tun_tun.py
```

Create a remote repo `tun-tun` on Github - https://github.com/new

```
➜  git remote add origin git@github.com:akshayaSalunke/tun-tun.git
```

```
➜  git remote -v
origin	git@github.com:akshayaSalunke/tun-tun.git (fetch)
origin	git@github.com:akshayaSalunke/tun-tun.git (push)
```

Start the ssh-agent in the background.

```
➜  eval "$(ssh-agent -s)"
Agent pid 5742
```

Add your SSH private key to the ssh-agent and store your passphrase in the keychain. 

```
➜  ssh-add -K ~/.ssh/id_rsa
```

Copy the SSH key to your clipboard.

```
➜  pbcopy < ~/.ssh/id_rsa.pub
```

Add New SSH key - https://github.com/settings/keys

Test your SSH connection

```
➜  ssh -T git@github.com
The authenticity of host 'github.com (192.30.255.113)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com,192.30.255.113' (RSA) to the list of known hosts.
Hi akshayaSalunke! You've successfully authenticated, but GitHub does not provide shell access.
```

```
➜  git push -u origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 311 bytes | 311.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:akshayaSalunke/tun-tun.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

## References

https://help.github.com/en/github/getting-started-with-github/create-a-repo

https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh

https://help.github.com/en/github/using-git/pushing-commits-to-a-remote-repository
