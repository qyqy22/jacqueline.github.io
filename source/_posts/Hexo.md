---
title: How To Build Hexo+Github
date: 2019-05-02 10:12:18
tags:
---
##  What is Hexo?
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Step
1.create new Repository in Github     
2.Install Tools      
3.Deploy Website   
4.Use Hexo    
5.Markdown Article   

### Create new Repository in Github
Once you've signed in,you'll create a new repository to get started.  
On the new repository screeen, you need to give this repository a special name to generate your website.   
![gitpagesname](/css/images/pictures/renameRepo.png)    
Your website's files will live in a repository named `username.github.io` （where 'username' is your actual GitHub user name）.click create repository.       
![githubpage](/css/images/pictures/githubpage.png)    
<!--more-->
### Install Tools Git
download [git](https://git-scm.com/). Test 'git' in command line weather installed succeed.    
connect git to github account.    
click right to open Git Bash  
![gitbash](/css/images/pictures/gitbash.jpg)    

set `user.name` and `user.email`      
```bash
git config --global user.name  
git config --global user.email  
```                     
    
ssh security file:  
```bash
ssh-keygen -t rsa -C
```             

enter three times and don't need to set up security password.
find id_rsa.pub in .ssh files, and copy content in id_rsa.pub  
![security](/css/images/pictures/security.jpg) 

setting github ssh security key    
![sshkey](/css/images/pictures/sshkey.png)   

Test github security key whether set up succeed in GitBash  
command line:  ssh git@github.com  
You don't need to enter your username and password when you git push a repository.   

### Install Tools Node.js    
download [Node.js](https://nodejs.org/en/).    
Test node.js   
command line:  node -V   
Test npm  
command line: npm  -V   
Hexo environment has been completed!!!   

### Install Hexo  
Create a new file, and you can named 'Blog'.    

command in the Blog file. Install Hexo  
```bash
D:\Blog> npm install -g hexo-cli 
```          

init blog page  
```bash
D:\Blog>hexo init blog   
```           

Test our blog whether create succeed, command three lines deparately   
new a blog article    
```bash
D:\Blog>hexo new myblog  
```    

generate files  
```bash
D:\Blog>hexo g   
```    

start local server  
```bash
D:\Blog>hexo s 
```    

ctrl + click url, and we can see our blog.

### Deploy Website 
config the _config.yml in the root blog.  
![gitpagesname](/css/images/pictures/config.jpg)  

connect Hexo to Github, This configuration can let Hexo to know where should deploy the project     
![gitpagesname](/css/images/pictures/deploy.png)    

Install git deploy plugin   
```bash
npm install hexo-deployer-git --save
```    

Then we test it, we command three lines.
clean publish     
```bash
D:\Blog>hexo clean    
```   

generate files  
```bash
D:\Blog>hexo g   
```   

deploy to github  
```bash
D:\Blog>hexo d   
```     

Open browser to put in `username.github.io`. You can find the website in github pages setting.     
Your blog is online.  

####  Resource: you can git push another branch 'hexo'    
####  deploy: you git deploy on branch 'master'     

### Using Hexo 
Directory structure
```bash
---_config.yml   globale configuration
---package.json  parameter and dependencies  
---scaffolds  stucture file 
---source    new blogs 
   --_posts    you can see new blogs .md files in this file
---themes   you can download themes and put it under this files
```     

####  Themes  (ejs &  stylus)   
[ejs](https://ejs.co/) is Embedded JavaScript templating.     
What is the "E" for? "Embedded?" Could be. How about "Effective," "Elegant," or just "Easy"? EJS is a simple templating language that lets you generate HTML markup with plain JavaScript. No religiousness about how to organize things. No reinvention of iteration and control-flow. It's just plain JavaScript.     
[stylus](http://stylus-lang.com/) XPRESSIVE, DYNAMIC, ROBUST CSS.  
Themes  directory structure    
```bash
---languages  languages files international 
---layout   pages layout files  .ejs files 
---scripts   Hexo scripts  
---source   resource files  including stylus files 
---_config.yml themes configuration file 
```  

###  Markdown Article 
[Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).   




