# housing-justice-ai
Legal information and case-preparation assistant for tenants, voucher holders, EHV participants, and housing justice support.
Step 1: Create the GitHub repository

Go to GitHub and do this:

Click the + sign in the top-right.
Click New repository.
Repository name:
housing-justice-ai
Description:
Legal information and case-preparation assistant for tenants, voucher holders, EHV participants, and housing justice support.
Choose Private for now.

Do not check README, .gitignore, or license yet, because your project already has files.

Click Create repository.

Step 2: Put the project folder on your computer

Download the project I made:

Download housing-justice-ai.zip

Unzip it. Put the folder somewhere simple, like:

C:\Users\YourName\Documents\housing-justice-ai
Step 3: Open the folder in VS Code

Open VS Code.

Click:

File → Open Folder → housing-justice-ai

Then open the terminal:

Terminal → New Terminal
Step 4: Create a .gitignore file

In VS Code, create a file named:

.gitignore

Put this inside it:

.env
.venv/
__pycache__/
*.pyc
.DS_Store
*.log
uploads/
case_files/
private_evidence/

This is important. Do not upload your API key, private court documents, private evidence, or personal case files to GitHub.

Step 5: Run these Git commands

In the VS Code terminal, type these one at a time:

git init
git add .
git commit -m "Initial commit for Housing Justice AI"
git branch -M main
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/housing-justice-ai.git
git push -u origin main

Replace this part:

YOUR-GITHUB-USERNAME

with your real GitHub username.

Example:

git remote add origin https://github.com/terrykno33/housing-justice-ai.git
Step 6: Check GitHub

Refresh your GitHub repository page.

You should see:

app.py
requirements.txt
README.md
.env.example
prompts/
data/

That means your project is officially in GitHub.

Important

Keep the repository Private while you are building it. Later, once you remove all personal information and private case details, you can decide whether to make it public for your portfolio.

For your first commit, use this:

Initial commit for Housing Justice AI
