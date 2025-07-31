# cintel-06-custom
Repo for 44630: Custom Interactive App

### Preliminary Setup Steps
### 1. Initialize
```
1. Click "New Repository"
    a. Generate name with no spaces
    b. Add a "README.md"
2. Clone Repository to machine via VS Code
    a. Create folder in "C:\Projects"
3. Install requirements.txt
4. Setup gitignore
5. Test example scripts in .venv
```
### 2. Create Project Virtual Environment
```
py -m venv .venv
.venv\Scripts\Activate
py -m pip install --upgrade pip 
py -m pip install -r requirements.txt
Retrieve installed items: !pip list
```
### 3. Git add, clone, and commit
```
git add .
git clone "urlexample.git"
git commit -m "add .gitignore, cmds to readme"
git push -u origin main
```
### 4. If copying a repository:
```
1. Click "Use this template" on this example repository (if it's not a template, click "Fork" instead).
2. Clone the repository to your machine:
   git clone example-repo-url
3. Open your new cloned repository in VS Code.
```
### 5. spaCy Specific Installs
```
1. pip install -U pip setuptools wheel
2. pip install -U spacy
3. python -m spacy download en_core_web_sm
```
### 6. HTML Export
```
import os os.system('jupyter nbconvert --to html python-ds.ipynb')
```
### 7. Specific Module 6 Imports
```
python -m pip install beautifulsoup4
python -m pip install html5lib
python -m pip install requests
python -m pip install spacy
python -m pip install spacytextblob
```
### 8. Exporting the app using `shinylive`
```
pip install shinylive
shinylive export . shinylive-app
cd shinylive-app
git init
git remote add origin https://github.com/dfintel25/cintel-06-custom.git
git checkout -b gh-pages
git add .
git commit -m "Deploy shinylive app"
git push -u origin gh-pages --force

Go to your repo: dfintel25/cintel-06-custom
    Navigate to:
    Settings → Pages
    Under "Build and deployment":
    Set Source to gh-pages branch
    Set the folder to / (root)
    Click Save
```
### 9. Connecting to ShinyApps.io
```
[ShinyApps.io](https://www.shinyapps.io/)
pip install rsconnect-python
rsconnect --version
rsconnect add --name dfintel25 --server shinyapps.io
rsconnect add --account dfintel25 --name dfintel25 --token 1877325D96D5F585F9E67F8AEC905F89 --secret()
cd ..
cd C:\Projects\cintel-06-custom
rsconnect add --name dfintel25 --server shinyapps.io ...
rsconnect deploy shiny . --name dfintel25 --title "Stock Explorer" --app-name stock-explorer
```
