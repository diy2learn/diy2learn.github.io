---
layout: page
#
# Content
#
subheadline: "Jekyll"
title: "My path to Jekyll"
teaser: "way to learn"
categories: 
  - thoughts
  - technics
tags:
  - jekyll, learn
---

Problem: I couldn’t push a new repository into my new github account newGit. I did clone an empty repository from newGit, into my computer.
I’m trying SSH keys:
Using the tutor: 
https://gist.github.com/jexchan/2351996
That didn’t work. 
"I had to change the [remote "origin"] / url field in my local .git/config to use the Host defined in .ssh/config in order for this to work, i.e.,

[remote "origin"]
url = git@github.com-activehacker:activehacker/gfs.gi”
if your ssh key is ~/.ssh/id_rsa_activehacker,add “-activehacker” in [remote “origin"] in your local .git/config. (modifiable with Vim)
I should have tried this but I didn’t have time
https://kev.inburke.com/kevin/multiple-github-ssh-accounts/

Now I’m following the official tutor from github:
Check if I have SSH key?  
ls -al ~/.ssh
# Lists the files in your .ssh directory, if they exist
https://help.github.com/articles/checking-for-existing-ssh-keys/

*) Check if SSH key is added into agent
# start the ssh-agent in the background
eval "$(ssh-agent -s)”
output: Agent pid 59566
ssh-add -l
output: 2048 a0:dd:42:3c:5a:9d:e4:2a:21:52:4e:78:07:6e:c8:4d /Users/you/.ssh/id_rsa (RSA)
https://help.github.com/articles/error-permission-denied-publickey/
**) Add SSH key if not done yet
$ ssh-add ~/.ssh/id_rsa
https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/
(Make sure that ssh-agent is started in the background)
***)Associate ssh-key to Github
# Copy ssh-key to clipboard
pbcopy < ~/.ssh/id_rsa_username.pub
# Go to Github setting->SSH and GPG keys -> New SSH key or Add SSH key
https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/
*V) Try connection to github by
ssh -vT git@github.com
https://help.github.com/articles/error-permission-denied-publickey/

v) If I try push with https protocol, I got “permission denied” error, due to github refuse to accept my push (some how) with my old github account (even though I tried every way to delete or overwrite git config user.name/user.email)
Finally, if I clone my repository using SSH protocol, then it work
a) Connect to github using SSH protocol
ssh -T -p22 git@github.com
b) clone the interested repository 
git clone git@github.com:username/repo.git
c) copy data into this cloned-repository
d) Add/commit/ push data to the git:
git Add . 
git commit -m “copy data in”
git push -u origin


 [1]: #
 [2]: #
 [3]: #
 [4]: #
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #