# Voluntold
Voluntold is a random person selector that ensures all options are picked before a duplicate can be picked again.  In other words, an option cannot be selected until every other option has been selected.  
Normal random generators select the same students over and over again, causing frustration and confusion in a classroom.  Voluntold works to fix that issue by preventing students from being selected again until everyone has gone through.  To make it simple for anyone to use, this guide includes instructions on how to set up and create your own version.

## Required
In order to create your own version of Voluntold, you must have the following items:
- Free GitHub Account
- Web browser/Internet Access
- Text Editor (recommended)

## Usage
This program is free to use under the MIT License, so feel free to use it however you would like.  
This template is set up for a single teacher in mind to make it easy to set up for new users.  It is possible for multiple teachers to use the same project, but it is recommended that each teacher keeps their own repository instead of having one set up to share. 

## Step 1: Forking the repository
In order to make this program customized for your class, go to the top of this page and click on the green button that says 'Use this template' or click on [this link](https://github.com/sheepman39/voluntold-template/generate).  
This will allow you to make a new repository (aka 'repo') where you can edit and customize your version of Voluntold.   To deploy this project in order for it to be used, we will be using [Github Pages](https://pages.github.com/), a free service included with every GitHub Account.  GitHub Pages makes it easy to deploy basic HTML applications like this one.

<br>

Name the repository that you just created "*username*.github.io" where *username* is your GitHub username.  It must be exactly the same or it will not work properly.  You can add a description if you would like, but it is not necessary.  
Next, mark the visibility of the project as Public so this page can be seen by anybody.  If you mark it as Private, GitHub will not publish your version of Voluntold.
Click on 'Create repository from template' and you will be directed to your new repository home page.

## Step 2: Editing files
Once you made your new repo, wait for about 5 minutes and then go to *username*.github.io, where *username* is your GitHub username.  Your version of voluntold should show up at the site.
However, the class names and students are not set up yet.  In order to set it up, we will have to edit the program.  This process has been made as simple as possible for new users.

<br>

First, on your repositories main page (this will be https://github.com/*username*/*username*.github.io), click on the file labeled `students.json`.  Next, you should see a file with a bunch of text in it.  On the right side of the screen will be a picture of a pen labeled `Edit this file`.  Click on the pen to edit.

<br>

We will go through the process of customizing step by step.  The second line should say something like `"firstHour": {`.  Please note that `firstHour` is in quotation marks. This is very important.  

<br>

### JSON syntax
Voluntold uses an object structure called json in order to make customizability easy and fast to use.  However, it is important to keep the structure of the file consistent.
Your file should have multiple segments that look like this: 
```json
    "firstHour": {
        "names": ["Faith", "Myrtle H.", "Tia", "Eric"],
        "extra": [],
        "className": "Spanish 1 1st H"
    },
```
Note that any name (firstHour, names, extra, className) is within quotation marks.  *When changing the name of anything, it is important to keep them within matching quotation marks.*
Commas, brackets, curly brackets, and colons should not be deleted or added randomly or else it will not work.  The next few sections will talk about what you can and cannot change.

<br>

Going to a json checker site like [jsonlint.com](https://jsonlint.com/) is a good way to check your json file.  If it is not correct, you can fix it by checking the red error message below the text box.

<br>

### Class Names
While we recommend keeping this label the same, feel free to change `firstHour` and the following hours to whatever name you would like **as long as it is only upper and lower case letters with no spaces or other symbols.**
There are six labels that are similar to `firstHour`.  If needed, change those as well depending on your preferences and class hours.  

<br>

### Adding additional classes
If you need to add a class hour, copy **all** of lines 2-6 and paste it in between lines 6 and 7.  Once you have the new class, you **must** change the name of the class and the students in it.  Duplicate class names are not allowed.

<br>

### Changing the names of students
In each of your class hour's, there is an indented section labeled `names`.  This is where you will input the names of each of your students.
Delete the default names within each of these so you can add your own.  Each one of the student's names must be in quotation marks with a comma separating them, as shown in the example above.  The last item of the list does not need to have a comma at the end.  Each of the names must be within the brackets [ ]. 

<br>

### Changing the text on the button
In each of your class hour's, there is an indented section labeled `"className": "<sample text>"`.  Change what is in the <> to the text you would like on the buttons that will be used to select which class you are choosing from.  
If this value is left blank or deleted, it will default to the name of the class hour you put down.

<br>

## Step 3: Commit your changes
After editing each of your classes to be the way you want them, scroll down on GitHub and select `commit directly to the main branch` and hit the green button that says `commit changes`.  This will save your changes and your site should be updated shortly.
Go back to your repository page (https://github.com/*username*/*username*.github.io) and refresh it.  On one of the top bars will be either an orange dot or a green check mark indicating if your site has been updated.
Once it has turned green (it may require a refresh to see the check mark) go to your site and refresh it.  Assuming everything works properly, you now have your customized version of Voluntold!  

<br>

## Troubleshooting
Here are some common issues that you may run into and how to fix them.

<br>

### 404: Page not found
If this shows up when trying to go to your site, make sure you are spelling everything exactly right.  The name of your repo must be exactly `*username*.github.io` where *username* is your GitHub username.  When deployed to your GitHub Pages site, the link will be `https://*username*.github.io/*username*/*username*.github.io`.
If you go to your repo Settings and click on `Pages`, you should see some other settings with this.  
Also, do not change any file names or the file structure of your repo.  If you do, you will not be able to deploy your site.

<br>

### SyntaxError: Unexpected token '' in JSON at position X
This error often means that there is a syntax error in your json file.  Check your json file and make sure it is formatted correctly.  
Once again, a json checker site like [jsonlint.com](https://jsonlint.com/) is a good way to check your json file.  If it is not correct, you can fix it by checking the red error message below the text box.  Usually an error like this will come from a missing comma, quotation mark, or bracket.  
If you are still having this error after a while, submit an [issue](https://github.com/sheepman39/voluntold-template/issues) on GitHub and include the JSON file.

<br>

### TypeError: Failed to fetch _
This error usually means that you are trying to view the site locally instead of hosting it on GitHub or the `students.json` file is renamed/deleted from your repository.  For security reasons, your browser will not allow you to view it locally so you must have it hosted on GitHub.  If you still have this error, double check that you have the `students.json` file in your repository.  If you are still having this error after a while, submit an [issue](https://github.com/sheepman39/voluntold-template/issues) on GitHub and include the link to your repository.
    
<br>

# Advanced Notes

If you are a developer that would like to take a look at the actual code running, you are free to do so and modify it however you would like.
The basic layout is in the `index.html` file.  The color scheme is within the `layout.css` files.  The core functions and buttons are in the `script.js` file.
None of these files should be edited unless you know what you are doing.  I have done my best to keep the code clean and commented so others can easily understand what is going on.  If you have any questions, please do not hesitate to submit an [issue](https://github.com/sheepman39/voluntold-template/issues) on GitHub and I will be happy to help.
