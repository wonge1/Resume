# **Guide for Publishing A Resume to Github Pages**

## **Introduction**

The purpose of this guide will be to walk you through the steps necessary to host a resume on a static site and deploy to Github Pages. This option gives your resume a more dynamic presentation that can be updated easily with changes or different styles.

## **Getting Started**

### **Prerequisites**
This guide will be written with the following assumptions, that a user has
- a resume in .md format
- a windows operating system
### **Tech Stack**
The tech stack will include
- Github Pages
- Jekyll
- Markdown
- Any IDE
## **Installation**

To install jekyll we will need to first download a couple things first. The first one will be Ruby. 
1. Head to https://rubyinstaller.org/. 
    * From there, install the recommended version 
    * Follow the along with the default download settings. 
    * When you click finish it will open up a new terminal for you to download 3 final items. You will want to follow the instructions to download each item in order from 1-3. 
    * Once done you can simply exit the terminal.

2. From here open a new terminal by typing into cmd into your windows search bar. 

3. Once there double check installations by using the following commands
```
gem -v 
```
and 

    ruby -v

if done correctly you will see version numbers.

4. Next will be to install Jekyll, which will be our static site generator, with the following command
```
gem install jekyll bundler
```
Once done you can double check the installation with 
    
    jekyll -v

## **Site Generation**

From here we will now be using the Jekyll to create our state site. This will give us an oppurtunity to see how everything will look locally before sending it off to be hosted on Github Pages.

1. With your terminal run the following command (foo is in place of your chosen site name)
```
jekyll new foo
```
2. Place your resume content below header in the default post in the _posts folder

By default a basic set of files will be generated for you. The folder **_posts** will be where you will want to place your content. However it will have to be formatted in the same way as the default post, with the Jekyll info included at the top and similar naming convention.

<p align="center">
  <img src="https://github.com/wonge1/Resume/blob/gh-pages/_img/JekyllPostInfo.PNG" alt="Jekyll Post Heading Example" width="300">
</p>

At this point you can move on to the next section if you wish to simply host your site on GitHub Pages, however if you would like to see what your site looks like locally continue in this section.

3. Navigate to the created folder with a terminal

4. Run the following command

```
bundle exec jekyll serve 
```

## **Setting Up GitHub Repository**

Before we can host anything we must first set up the repository. This is essentially a folder of files that is stored on Github's servers.

1. First head to https://github.com/new
2. Name this repo whatever you would like, by default all the settings should be fine for this process, then click create.
3. In your Jekyll folder, you will have to edit your baseurl variable in the ```config.yml``` file to be the name of your repo.
4. In your terminal navigate to your Jekyll folder
5. Run the following commands
```
git init
git checkout -b gh-pages
git add .
git commit -m "initial commit"
git remote add origin https://github.com/USERNAME/REPONAME.git
git push origin gh-pages
```
These commands from top to bottom do the following
-   make the folder you are in a github repo
-   create a branch called gh-pages
-   add all your current files to a commit
-   commit your changes so they are remembered
-   connect to your created repository
-   then push your commit to the repository

At this point GitHub should be able to identify the resources you pushed and create the site automatically. You can find your url by going to your repo settings and then heading to the pages tab.

<p align="center">
  <img src="https://github.com/wonge1/Resume/blob/gh-pages/_img/Url.PNG" alt="Pages Url Location" width="700">
</p>

## **FAQ**

**Q** &nbsp; Why does Ruby/Gem/Jekyll -v return a not found error even after I downloaded them?

**A** &nbsp; This can occur when using an older terminal. If this is the case, then it can be resolved by simply closing your current terminal, opening a new one, and then repeating the command.

---

**Q** &nbsp; Why should I use Markdown?

**A** &nbsp; The .md format enables you to make many dynamic changes like Word might, but all within the file itself in a format designed for the web with readable syntax. In addition, the format is extremely malleable, being able to be changed to .html or .pdf very easily.

---

**Q** &nbsp; Why did my website fail to run?

**A** &nbsp; There could be many answers here, but to best diagnose it head to the GitHub Actions tab. There you can observe your workflow and see more details on why your site might have failed.

<p align="center">
  <img src="https://github.com/wonge1/Resume/blob/gh-pages/_img/ActionsTab.PNG" alt="Workflow Location" width="700">
</p>

## **More Resources**
Mike Dane's Guide to Jekyll: https://www.youtube.com/watch?v=T1itpPvFWHI

A General Readme Template: https://github.com/PurpleBooth/a-good-readme-template/blob/main/README.md 

## **Acknoledgements**