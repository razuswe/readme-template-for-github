Table of Contents
1.	How to install & configure git on ubuntu?
2.	How to connect repo with github or bitbucket?
3.	For connected repo.
4.	How to start clone project?
5.	How to create, merge & delete branch?
6.	gitignore
7.	gitattributes
8.	requirements.txt
1. How to install & configure git on ubuntu?
# Install git

$ sudo apt-get update
$ sudo apt-get install git

$ git --version

# Configure git’s settings

$ git config --global user.name "razuswe"
$ git config --global user.email "swe.razu@gmail.com"
2. How to connect repo with github or bitbucket?
# To create a new repo on github or bitbucket.
# Open terminal & change the current working directory to your local project.

$ git init

$ git status
$ git add (file name.py) or $ git add .
$ git commit -m "update razu's project"

$ git remote add origin (repository URL)
 
$ git push origin master
3. For connected repo.
$ git status
$ git add (file name.py) or $ git add .
$ git commit -m "update rony's project"
$ git push origin master
4. How to start clone project?
1. git clone...

2. create & active virtual environment.

$ virtualenv venv
$ source venv/bin/activate

3. Install all the requirements by following command from your terminal:

$ pip install -r requirements.txt
5. How to create, merge & delete branch?
1. How to create a new branch?

# To create branch
$ git branch Rony

# To check branch
$ git branch 
* master
 Rony

# To active branch
$ git checkout shoriot


2. How to merge a branch?

### শুধু মাত্র master branch থেকেই merge করা যাবে, অন্য কোনো branch থেকে merge করা যাবে না।
### merge করার সময় অবশ্যই master branch active থাকতে হবে।
### যেই branch merge করতে চাই, সেই branch এর নাম দিতে হবে git merge লেখার পর
$ git checkout master () 
$ git merge Razu

### pull করা লাগবে, যদি কোনো branch এর কোড নিজের লোকাল মেশিনে আনতে চান। 
$ git pull origin Rony # যেই branch থেকে pull করবা সেই branch এর নাম।

### যেকোন branch থেকে pull করার পর নিম্মের কোড ইউস করতে হবে,
$ git pull --rebase origin Rony(branch name)


### যেই  branch এ কোড push করবা সেই branch active করে কাজ করতে হবে।
$ git status
$ git add (file name.py) or $ git add .
$ git commit -m "update razu's project"
$ git push origin shoriot


3. How to delete branch?

$ git branch -D (branch name) 
6. gitignore
.gitignore

*.pyc
*~
__pycache__
venv
db.sqlite3
/static
7. gitattributes
.gitattributes

*.html linguist-language=Python
*.css linguist-language=Python
*.js linguist-language=Python
8. requirements.txt
$ pip freeze > requirements.txt

This will create requirements.txt file.

