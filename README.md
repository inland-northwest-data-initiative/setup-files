# Github Configuration
## Setup Personal Access Token
1) Setup a personal access token as follows
- In the upper-right corner of any page, click your profile photo, then click Settings.
- In the left sidebar, click Developer settings.
- In the left sidebar, click Personal access tokens.
- Click Generate new token. Give your token a descriptive name.
- Select the scopes, or permissions, you’d like to grant this token. To use your token to access repositories from the command line, select repo.
- Click Generate token.
- Copy the token to your clipboard. For security reasons, after you navigate off the page, you will not be able to see the token again.

# RStudio Server configuration
## Update your password
1) Login to RStudio Server using the supplied username and password
2) In the bottom left window, go to the terminal tab to change your password  
```passwd```  
3) Enter the old password and new password (please use a good password here)
4) Go to the top right to logout and log back in using the new password

## Setup Github user and clone the repo
1) Setup the github user by going to the bottom left window and entering the following commands in the terminal tab. 
```git config --global user.name 'Jane Doe'```  
```git config --global user.email 'jane@example.com'```   
```git config --global --list```

2) Clone github repository as project
- Go to File > New Project > Version Control > Git
- In “Repository URL”, paste the URL of your new GitHub repository (in this case https://github.com/inland-northwest-data-initiative/inland-northwest-data-initiative.github.io.git)
- Leave "Project directory name" blank
- Enter the desired folder to house the project (leaving this as ~ should put the website in your home directory which is fine)

## Serve site locally
1) First of all, note that you should be in the git project you cloned in the previous step. To get back to this point in the future, you can just select open project from the RStudio menu and open the project.
2) For the first use, install hugo by entering the following in the bottom left window R console tab
```blogdown::install_hugo()```
3) At this point, you should be able to serve the site locally. You can go to the addins menu and select "serve site" which will open the site locally in the preview pane. You can click on the expand button to open the site in a browser, which should look identical to how the live site will appear.
4) Things at this point should be looking very similar to what Vivek demonstrated at the last meeting as far as adding blog posts, pages, etc.

## Make some changes and push them
1) Make some changes to readme.md or whatever file you choose.
2) Go to "Git" tab in the environment window (top right) and select the updated file as "Staged"
3) Press the commit button, enter commit message, click commit and then close
4) Select "Push" and enter Github username and *personal access token* for the password

## Pull request
1) Very simple, go to Git menu item and choose "Pull Branches" *while in your project*

## Shiny server (still needs work)
1) Create new repository for shiny apps
2) Create new project as above in shiny server folder
3) Pull request from github to update shiny server code
