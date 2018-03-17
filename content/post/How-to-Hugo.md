---
title: "How to Hugo"
date: 2018-03-16T23:41:07+01:00
draft: true
---

👋 Hello world! this is my first post with [**Hugo**](https://gohugo.io/) and i want to show you the steps to install and deploy your static web site on Github Pages(😸).
You must have installed this applications:

	- Homebrew
	- Git

### Install Homebrew
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
### Install Git
```bash
$ sudo apt-get install git-all
```
###Install Hugo
Create a static site using the framework Hugo using a theme:

```bash
brew install hugo
```

To verify your install:

```bash
hugo version
```
##Create a New Site

creating a new site:

```bash
hugo new site YOUR_PROJECT_NAME
```

##Add a Theme
You can look for free themes in [themes.gohugo.io](themes.gohugo.io):

```bash
cd YOUR_PROECT_NAME/

cd themes/

git clone GIT_HUB_REPOSITORIE.GIT
```

At this point you have a static web site with a really beautiful theme 😄.

##Add Some Content
```bash
hugo new post/POST_NAME.MD
```
With `.md`extension you can write your post using [_Markdown_](https://es.wikipedia.org/wiki/Markdown).

Now, start Hugo server with drafts enabled (this is very important).

When you create a post you must change `draft : true`to `false`.

To start a hugo server;

```bash
hugo server -D

Started building sites ...
Built site for language en:
1 of 1 draft rendered
0 future content
0 expired content
1 regular pages created
8 other pages created
0 non-page files copied
1 paginator pages created
0 categories created
0 tags created
total in 18 ms
Watching for changes in /Users/bep/sites/quickstart/{data,content,layouts,static,themes}
Serving pages from memory
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop

```
**Navigate to your new site at [http://localhost:1313/](http://localhost:1313/)**.

##Customize your Theme


[Hugo Themes](https://themes.gohugo.io/)

This part you must go to the theme creator documentation a edit de `config.toml`

```bash
  title = "facebook"
  url = "https://www.facebook.com/nickname"
  icon = "fa-facebook-square"
  footer = true
  sharethis = true
  network = "facebook"

```

##Deploying on Github Pages

Follow this instructions:

Create a new repo on github your_name_project (this folder must contain our blogs archives)
Create a new repo with this name: **USERNAME.github.io**

Go to yout project folder

Add a remote origin

```bash
git remote origin YOUR_NAME_REPO.GIT
git pull origin master

```
Edit .gitignore and add `public/`

Then

```bash
git add .
git status
```
You must see new file .gitignore

```bash
git commit -m "First commit"
git push origin master
```
At this point you should have your project uploaded on yout new repo. 🖥️

Now you have to clone your **USERNAME.github.io** on a new folder called **Username.girhub.io**

Go to USERNAME.github.io/

```bash
git clone USERNAME.github.io
```
in the same folder:
```bash
git pull origin master
```
Back to the Project folder:

```bash
hugo -d ../../USERNAME.github.io

```
Go to **USERNAME.github.io/**
```bash
git add --all
git commit -m "First Upload"
git push origin master
``

Go to your browser and write USERNAME.github.io and 💥

Your static web site is online!
