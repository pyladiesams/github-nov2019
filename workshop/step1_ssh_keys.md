## Step 1: SSH keys.
Not required, but with SSH keys make your pushes easier.

SSH = "secure shell", this protocol allows you to securely send your commits without explicit entering the password.

## Create SSH keys.

* Mac (also has to work with Ubuntu)
1.
` cd ~/.ssh/`
If you don't have this directory, you can create it:
```
cd ~; mkdir .ssh
```

2. Check you're in a right directory run `pwd` command, you should see something like:
```
/Users/olgas/.ssh
```
3. Check if you already have `id_rsa` and `id_rsa.pub` files. You can check it with command `ls` in your `.ssh` folder.
If you don't have them you have to create them using the tool `ssh-keygen`.
It will ask you for name of the file where you want to store a keys and a password. This password is *not* supposed to be the same as password to your GitHub account. (To simplify I would suggest to use an empty passphrase)

In the output you should see something like
```.ssh olgas$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/olgas/.ssh/id_rsa): id_rsa_example
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in id_rsa_example.
Your public key has been saved in id_rsa_example.pub.
The key fingerprint is:
SHA256:eGTtC+KcW8Yn3pWD3o1TIzeJEjuux8fCDgnrhvDhaLQ olgas@Olgas-MacBook-Pro.local
The key's randomart image is:
+---[RSA 2048]----+
|                 |
|         .       |
|        o .      |
|       + ..      |
|      + S .o . . |
|  o .o B o+oo.*  |
| . * o= B+++++ o |
|  E +..= **o++   |
| .   .o o++oo..  |
+----[SHA256]-----+
```
Files with names `id_rsa_example` and `id_rsa_example.pub`
* Don't share content of `id_rsa_example` with anyone!*
4. You will need content of `id_rsa_example.pub` file.
* Windows
[How to create ssh key](https://www.digitalocean.com/docs/droplets/how-to/add-ssh-keys/create-with-putty/)

## Put the key to your GitHub account

1. Go to your profile -> Settings -> SSH and GPA keys
2. Press the `New SSH key` button and paste content of `.pub`. For a title you can use anything that will help you to recognize where this key came from.
3. GitHub will ask your password for confirmation.  

This is it! You have a ssh key connected to your account. Now GitHub "knows" your machine and you can push commits from it without a password.
