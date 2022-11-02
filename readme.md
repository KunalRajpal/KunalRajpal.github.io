# Host a resume using GitHub Pages

![](Screen Recording 2022-11-01 at 11.59.49 PM.gif)

## Purpose

Practical steps to format and host a resume using a a lightweight markup language, and a Static Site Generating Tool. We are going to be using Markdown, a Markdown editor, GitHub Pages, and Jekyll. Further, this document will also entail general principles of current Technical Writing, as explained in Andrew Etter’s book Modern Technical Writing and relate to the practical steps which we are going to follow. 

## Table of Contents

+ Prerequisites
+ Instructions
+ More Resources
+ Authors and Acknowledgements
+ FAQs
### Prerequisites

You will need these before you can follow this tutorial

- **Resume formatted in Markdown**

	Please have a resume formatted in any lightweight markup language.

	Markdown, as described by Etter is, "simultaneously incredible and infuriating." It is also the most widely used markup language with the cleanest syntax, I recommend using Github flavoured Markdown for this tutorial.

	A Tutorial on how to use Markdown can be found in the More Resources Section.

- **Markdown Editor**

	A basic markdown editor is required, Andrew Etter suggests [Markdown Pad](http://www.markdownpad.com/) for Windows or [iA Writer](https://ia.net/writer) for Mac.
	
	For Simplicity purposes I am using [Visual Studio Code](https://code.visualstudio.com/Download) since it has cross platform functionality.

- **Git command line tools**

	You can use [this](https://github.com/git-guides/install-git) guide to install git on your device.

### Instructions

#### Preparing for Installation

1. **Making a GitHub Account**

	GitHub is the most widely Distributed Version Control. According to Etter, "For technical writers, the most important reason to use DVCS is that developers prefer them."  DVC's like GitHub help us keep track of our progress and facilitate multiple authors, including developers and users. To create an account on GitHub:
	* Go to [GitHub](https://github.com/) and click on the sign up button 
	* Choose your desired email, an unique username and a strong password
	* you should now have a working GitHub account. signIn to the account you just made to follow along!

2. **Creating a Repository**

	Create a new Repository on your account:
	* Click on the button that says ***new*** on the left side of your page to create a new Repository.
	* Enter the repository name as username.github.io for example: `KunalRajpal.github.io`
	* you can add an optional description.
	* You have the choice to make your repository Public or Private. I chose the Public option so people can discover my resume/portfolio.
	* Do not initialize the Repository with a readme.

3. Uploading your Resume
	You can add your Markdown formatted Resume to your Repository in this step. 
	* Go to the Repository you just created and locate the add file button which should be located on the right side of your screen
	* Upload your resume with the name `index.md`
	* Commit your changes, you can include a commit message if you like

#### Installing Dependencies

In this section we will install the software dependencies required to run Jekyll. This section is divided into two sections, one for Mac and one for Windows.

##### MacOS

1. We will start by installing XCode if it isn't already installed. Go to App Store and install X-code

2. After that we install Homebrew. Homebrew is a package manage for MacOS and it "installs the stuff that you need that Apple didn't." Open the Terminal on your device and paste following code in it:

	`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

3. After installing homebrew we need install ruby. Ruby is the programming language in which jekyll is written. Install ruby through homebrew package manager by running the following code in your terminal.

	`brew install ruby`

4. after that we are ready to install jekyll. We do so through something called gem. Install the jekyll gem

	`gem install jekyll bundler`

7. You can check if Jekyll has been installed properly by using:

	`jekyll -v`

##### Windows

1. We will be using git-bash to install dependencies on your Windows device. If you do not already have that you can download it [here.](https://git-scm.com/downloads)

2. Explain Chocolatey program manager on your device using the command prompt:

	`@powershell -NoProfile -ExecutionPolicy unrestricted -Command "(iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))) >$null 2>&1" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin`

3. Now your device should have the a package manager Chocolatey and git bash installed. We will be using both those tools moving forward. 

4. Open the git bash and run the following code to install ruby:

	`choco install ruby -y`

4. Restart your git-bash

5. Now ruby should be working properly on your device. We no install jekyll. Run this code in your git bash:

	`gem install jekyll bundler`

6. You can check if Jekyll has been installed properly by using:

	`jekyll -v`

#### Setting up Static website

Now you have installed everything required to run jekyll and start making websites. We will now set up our static website

1. Open the terminal on your device and Change Directory or `CD` to your desired location. This is where the files of your website will be saved.

2. I will go to the folder where I have saved the assignment 2 for my technical communicational class. This is the code i used in my terminal:
	
	`cd Desktop/Fall22/3040/A2/`

3. Here we will initiate our new static website.

4. But first we need to connect this to the git repository we created.

5. Create a folder named after your github repository: `KunalRajpal.github.io`. We will clone our GitHub repository here.

6. `CD` into the directory you just created.

7. Now head to [GitHub](https://github.com/) and to the repository we created earlier. click on the green code button and copy the link from there. 

8. Now clone your git repository using:
	`git clone <url>`

9. Now we can create our static website

	`jekyll new KunalRajpal.github.io`

10. Notice that *KunalRajpal.github.io* is also the name of the repository I created earlier.

11. This should add new files into your repository. 

12. Push your code to GitHub using:

	``` 
	git add .
	git commit -m "Initial commit"
	git push
	```

13. That is it! You can head to your website which will now be using hosting your resume!


##  More Resources

1. Head to this [tutorial](https://www.markdowntutorial.com) to learn markdown.
2. [This](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS) is a very useful resources by Andrew Etter to understand different principles of Modern Technical Writing.
3. For creative themes head to [this](https://jekyllthemes.io) website. 
##  Authors and Acknowledgements

* Written by: ***Kunal Rajpal***
* Edited by: Noah Curoe, Kunal Rajpal, Tristan Dyck

##  FAQs

* **Why is Markdown better than a word processor?**

	Markdown is used for basic syntax formatting and is incredibly lightweight. It is easy to read by humans and easy for machines to convert into XML files.
* **How can I update my resume?**

	By editing the `index.md`
