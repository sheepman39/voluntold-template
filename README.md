# voluntold
Voluntold is a program that allows teachers to automatically pick a student in a class and have everyone go through the list before someone else can be selected again.  Normal random generators will keep picking the same students over and over and this program solves that issue.  It is customizable and simple to use.

## Required
In order to use your own version of Voluntold, you must have the following items:
- GitHub Account
- Web browser/Internet Access
- Text Editor (recommended)

## Usage
This program is free to use under the MIT License, so feel free to use it however you would like.  
This template is set up for a single teacher in mind to make it easy to set up for new users.  It is possible for multiple teachers to use the same project, but it is recommended that each teacher keeps their own repository instead of having one shared. 

## Step 1: Forking the repository
In order to make this program your own version for your class, go to the top of this page and click on the green button that says 'Use this template' or click on [this link](https://github.com/sheepman39/voluntold-template/generate).  
This will allow you to make a new repository (repo) where you can store all of your classes.   For this project to be available, we will be using [Github Pages](https://pages.github.com/), a free service included with every GitHub Account.  It makes it easy to deploy basic HTML applications like this one.
Name the repository that you just created <*username*.github.io> where *username* is your GitHub username.  It must be exactly the same or else it will not deploy properly.  You can add a description if you would like, but it is not necessary.  
Next, mark the visibility of the project as Public so this page can be seen by anybody.  If you mark it as Private, GitHub will not publish your version of Voluntold.  Congrats!  You just completed step 1!

## Step 2: Editing files
Once you made your new repo, wait for about 5 minutes and then go to *username*.github.io, where *username* is your GitHub username.  Your version of voluntold should show up at the site.
However, the class names and students are not correct for you.  In order to customize it, we will have to edit the program.  This process has been made as simple as possible for new users.
First, on GitHub, click on the file labeled `students.json`.  Next, you should see a file with a bunch of data in it.  On the right side of the screen will be a picture of a pen labeled `Edit this file`.  Click on the pen to edit.
We will go through the steps of customizing step by step.  The second line should say something like `"firstHour": {`.  Please note that `firstHour` is in quotation marks. This is very important.  

### JSON syntax
Voluntold uses a file structure called json in order to make customizability easy and fast to use.  However, it is important to keep the structure of the file consistent.
Your file should have multiple segments that look like this: 
```json
    "firstHour": {
        "names": ["Camdin", "Olivia B", "Ashanti", "Abbie"],
        "extra": [],
        "className": "Spanish 1 1st H"
    },
```
Note that any name (firstHour, names, extra, className) is within quotation marks.  *When changing the name of anything, it is important to keep them within quotation marks.
Commas, brackets, curly brackets, and colons should not be deleted or added randomly or else it will not work.  The next few sections will talk about what you can and cannot change.

### Class Names
While we recommend keeping this label the same, feel free to change `firstHour` to whatever name you would like **as long as it is only upper and lower case letters with no spaces or other symbols.**
There are six labels in a similar way as `firstHour`.  If needed, change those as well depending on your preferences and class hours.  

### Adding additional classes
If you need to add a class hour, copy **all** of lines 2-6 and paste it in between lines 6 and 7.

### Changing the names of students
In each of your class hour's, there is an indented section labeled `names`.  This is where you will input the names of each of your students.
Delete the default names within each of these so you can add your own.  Each one of the student's names must be in quotation marks with a comma separating them, as shown in the example above.  The last item of the list does not need to have a comma at the end.  Each of the names must be within the brackets []. 

### Changing the text on the button
In each of your class hour's, there is an indented section labeled `"className": "<text that will appear on the button>"`.  Change what is in the <> to the text you would like on the buttons that will be used to select which class you are choosing fro.  
If this value is left blank or deleted, it will default to the name of the class hour you put down.

## Step 3: Commit your changes
After editing each of your classes to be the way you want them, scroll down on GitHub and select `commit directly to the main branch` and hit the green button that says `commit changes`.  This will save your changes and your site should be updated shortly.
Go back to your repository page (github.com/*username*/*username*.github.io) and refresh it.  On one of the top bars will be either an orange dot or a green check mark indicating if your site has been updated.
Once it has turned green (it may require a refresh to see the check mark) go to your site and refresh it.  Assuming everything works properly, you now have your customized version of voluntold!  

# todo: Add common errors and advanced settings