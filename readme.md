# Host a resume using GitHub Pages

## Purpose

Practical steps to format and host a resume using a a lightweight markup language, and a Static Site Generating Tool. We are going to be using Markdown, a Markdown editor, GitHub Pages, and Jekyll. Further, this document will also entail general principles of current Technical Writing, as explained in Andrew Etter’s book Modern Technical Writing and relate to the practical steps which we are going to follow. 

## Table of Contents

### Prerequisites

- **Resume formatted in Markdown:** Please have a resume formatted in any lightwieght markup language, we recommend using Markdown. A Tutorial on how to use Markdown can be found in the More Reources Section. 
- **Markdown Editor:** A basic markdown editor is required, Andrew Etter suggests [Markdown Pad](http://www.markdownpad.com/) for Windows or [iA Writer](https://ia.net/writer) for Mac. For Simplicity purposes I am using [Visual Studio Code](https://code.visualstudio.com/) since it has cross platform functionality. 

### Instructions

#### Preparing for Installation

1. **Making a GitHub Account**
		GitHub is the most widely Distributed Version Control. According to Etter, "For technical writers, the most 	important reason to use DVCS is that developers prefer them."  DVC's like GitHub help us keep track of our progress and facilitate multiple authors, including developers and users. To create an account on GitHub: 
		* Go to [GitHub](https://github.com/) and click on the sign up button 
		* Choose your desired email, an unique username and a strong password
		* you should now have a working GitHub account. signIn to the account you just made to follow along!
2. Creating a Repository
	Create a new Repository on your account:
	* Click on the button that says ***new*** on the left side of your page to create a new Repository
	* Enter the repository name as username.github.io for example: KunalRajpal.github.io
	* you can add an optional description
	* You have the choice to make your repository Public or Private. I chose the Public option so people can discover my resume/porfolio 
	* Do not initialize the Repository with a readme

3. Uploading your Resume
	You can add your Markdown formatted Resume to your Repository in this step. 
	* Go to the Repository you just created and locate the add file button which should be located on the right side of your screen
	* Upload your resume 
	* Commit your changes, you can include a commit message if you like

#### Installing Dependencies 

In this section we will install the software dependencies required to run Jekyll. This section is divided into two sections, one for Mac and one for Windows. 

##### MacOS

1. We will start by installing XCode if it isn't already installed. You can do so by going to the AppStore and searching for XCode
2. After that we install Homebrew. Homebrew is a package manage for MacOS and it "installs the stuff that you need that Apple didn't." Open the Terminal on your device and paste following code in it:
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
3. Install chruby and ruby-install with Homebrew, you can do that by using:
`brew install chruby ruby-install xz`
4. Install the latest stable version of Ruby:
`ruby-install ruby`
5. Once that is done, configure your shell with:
`echo  "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh"  >> ~/.zshrc` 
` echo  "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh"  >> ~/.zshrc `
` echo  "chruby ruby-3.1.2"  >> ~/.zshrc # run 'chruby' to see actual version`
6. After installing Ruby with chruby, install the latest Jekyll gem
`gem install jekyll bundler`
7. You can check if Jekyll has been installed properly by using:
`jekyll -v`

##### Windows

1. We will be using git-bash to install dependecies on your Windows device. If you do not already have that you can download it [here.](https://git-scm.com/downloads)
2. Explain Chocolatey program manager on your device using the command prompt:
`@powershell -NoProfile -ExecutionPolicy unrestricted -Command "(iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))) >$null 2>&1" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin`
3. Using git-bash install ruby using Chocolatey:
`choco install ruby -y`
4. Restart your git-bash
5. Install Jekyll using:
`gem install jekyll bundler`
6. You can check if Jekyll has been installed properly by using:
`jekyll -v`

#### Setting up Jekyll
1. CD to the target location for your static website
2. `jekyll new KunalRajpal.github.io` Notice that *KunalRajpal.github.io* is also the name of the repository I created 
3. CD into the directory you just created 
4. `bundle exec jekyll serve --watch` <br/> Here the serve tag runs the website locally and the --watch tag asks jekyll to watch for any changes to wesbite files
5. This starts a website on our local host and a port number. Your terminal will give you the server address running your website, such as `http://localhost:4000/`
6. You can go to this address to check out your website
7. Jekyll is now being run from this command line window, so you’ll need to open a new command line window if you want to type other commands while your local site is still accessible to you
8. 


#### Hosting on GitHub Pages

##  More Resources

##  Authors

##  Acknowledgements

##  FAQs