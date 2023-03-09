# **Guide for Publishing A Resume to Github Pages**

## **Introduction**
---
The purpose of this guide will be to walk you through the steps necessary to host a resume on a static site and deploy to Github Pages. This option gives your resume a more dynamic presentation that can be updated easily with changes or different styles.

## **Getting Started**
---
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
---
To install jekyll we will need to first download a couple things first. The first one will be Ruby. 
1. Head to https://rubyinstaller.org/. 
    * From there, install the recommended version 
    * Follow the along with the default download settings. 
    * When you click finish it will open up a new terminal for you to download 3 final items. You will want to follow the instructions to download each item in order from 1-3. 
    * Once done you can simply exit the terminal.

From here open a new terminal by typing into cmd into your windows search bar. Once there double check installations by using the following commands

    gem -v 

and 

    ruby -v

if done correctly you will see version numbers.

2. Next will be to install Jekyll, which will be our static site generator, with the following command

    * gem install jekyll bundler

Once done you can double check the installation with 
    
    jekyll -v

## **Site Generation**

From here we will now be using the Jekyll to create our state site. This will give us an oppurtunity to see how everything will look locally before sending it off to be hosted on Github Pages.

1. With your terminal run the following command

foo is in place of your chose site name

    jekyll new foo

2. Place your resume.md into the _posts folder

By default a basic set of files will be generated for you. The folder **_posts** will be where you will want to place your resume.md. However it will have to be formatted in the same way as the default post, with the Jekyll info included at the top

<p align="center">
  <img src="./_img/JekyllPostInfo.png" alt="Jekyll Post Heading Example" width="300">
</p>


## **Setting Up GitHub Repository**

From here we will now be using the Jekyll to create our state site. With your terminal run the command

    jekyll new foo


## **Acknowledgements**
Mike Dane
https://www.youtube.com/watch?v=T1itpPvFWHI


https://github.com/PurpleBooth/a-good-readme-template/blob/main/README.md 