# How to use GitHub

## Register a GitHub account

* Use your email address to register a GitHub account, make sure to write down your password

  http://github.com/

## Set up key access your GitHub from your Linux 

* check if you already have a public key

```
# ls ~/.ssh/
```

* if necessary, create a SSH public key

```
# ssh-keygen

# cat ~/.ssh/id_rsa.pub
```

* add the public key your GitHub account under Settings -> "SSH and GPG keys" -> "New SSH key"

## Create a private GitHub repository

* Create a new repository, make sure to mark it as a private repository

## Work with your GitHub repositoy 

Go to your GitHub repositoy page and click on "Clone or download" button, copy the repository link, here
we use our lab repository as example,

```
git@github.com:computerlabtx/lab.git
```

clone a copy of the repository at a local directory in your Ubuntu VM, for example, create a new local directory
under your home directory

```
# cd ~/
# mkdir git
# cd git
# git clone git@github.com:computerlabtx/lab.git
# cd lab/
# ls -la
```

Note some git related files and directory at top of the local repository copy.

Now you may add/create files under your local repository, try create a file, name

```
# vi sample.txt
```

put in some statements like "this is a sample file for my GitHub"

Now we check in the new file, make sure you goto top of your repository directory 

```
# cd ~/git/lab
# git add .
# git commit -m "add sample.txt file to my repository" . 
```

This will check in your changes into your local source control, but not yet available
on GitHub.  You may continue to change/add in your local repository, say, we add
one more file,

```
# vi sample2.txt
# ls -al
```

Next we will check in the sample2.txt and also push all the changes we made locally
to the repository to GiyHub

```
# cd ~/git/lab
# git add .
# git commit -m "add sample2.txt file" .
# git push
```

If everything goes well, all your local changes should have been push up into GitHub.
You may check your repository page on GitHub where you should see two new files,
sample.txt and sample2.txt

## What you will use GitHub repository for

We will use the GitHub repository to save all your project works from the class, that includes
any notes you will take for the class.  By doing so, you will always have a copy of your work
in the cloud and you can have access to your work from other places if you're not on your 
VM.  And it provides as a safety if in any case you lost your VirtualBox and/or Ubuntu. 

