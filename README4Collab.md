
# CSIR LimeSurvey Customization (`limesurvey-csir`)

This repository is a fork of **LimeSurvey** for CSIR customizations.  

- **Author/Owner:** [@PaakowTronics](https://github.com/PaakowTronics)  
- **Primary working branch:** `csir-custom`  
- **Tooling:** VS Code + Git/GitHub (no XAMPP instructions here)


## 0) Prerequisites
- Git installed → `git --version`
- VS Code installed
- GitHub account with **Write** access to this repo
- XAMPP/WAMP for local testing  
- **VS Code** is recommended because `.gitignore` is already configured.  
  *If you prefer another editor, let the team know.*

 
 ## 1) First-time Setup (Collaborators)

> All instructions should be done in **bash**.  
> Change terminal to bash and set as default.


# 1) Clone the repo
```    
 git clone https://github.com/PaakowTronics/limesurvey-csir.git

 cd limesurvey-csir
```
# 2) Switch to the working branch
     git checkout csir-custom

# 3) Identify yourself to Git (do once per machine)
     git config --global user.name "Your Full Name"
     git config --global user.email "your-email@example.com" 


✅ Always work on csir-custom unless the project lead asks otherwise.
## 2. Daily Workflow (Before Editing)
Always pull the latest changes first:

    git pull origin csir-custom
## 3. Making Changes and Saving your Work

- Open the folder in VS Code.

- Make your edits (PHP, Twig, CSS, JS, etc.).

- Stage → Commit → Push:
```
    git add .

    git commit -m "Short, clear summary of what you changed"

    git push origin csir-custom

```
✅ Be specific in your commit messages (mention files/areas when useful).
## 4. Recommended Repo Structure to Edit

Admin theme (safe to customize):

    themes/admin/csir_admin/
(duplicate of default admin theme — safe to modify)

Optional survey theme (if used):

    themes/survey/csir_fruity/ 
(or your chosen name)

⚠️ Avoid editing core application files unless overriding via proper theme/view overrides.
Theme copies are not overwritten by LimeSurvey updates.
## 4. Recommended Repo Structure to Edit

Admin theme (safe to customize):

    themes/admin/csir_admin/
(duplicate of default admin theme — safe to modify)

Optional survey theme (if used):

    themes/survey/csir_fruity/ 
(or your chosen name)

⚠️ Avoid editing core application files unless overriding via proper theme/view overrides.
Theme copies are not overwritten by LimeSurvey updates.
## 5. Handling Merge Conflicts

If git pull shows conflicts, VS Code will mark them with:

    <<<<<<< HEAD
    your local change
    =======
    incoming change
    >>>>>>> origin/csir-custom


Manually choose the correct lines and remove the markers.

Then run:

    git add .
    git commit -m "Resolve merge conflicts in <file>"
    git push origin csir-custom


ℹ️ If you’re unsure, choose Option A and let the project lead manage upstream updates.
## 6. Optional: Feature Branches + PRs

For larger changes, create a feature branch:

# Create branch from csir-custom
    git checkout csir-custom
    git pull origin csir-custom
    git checkout -b feature/admin-login-header

# Work, then save
    git add .
    git commit -m "Add CSIR header to admin login"
    git push origin feature/admin-login-header

Then open a Pull Request to csir-custom on GitHub for review.
## 6. Optional: Feature Branches + PRs

For larger changes, create a feature branch:

# Create branch from csir-custom
    git checkout csir-custom
    git pull origin csir-custom
    git checkout -b feature/admin-login-header

# Work, then save
    git add .
    git commit -m "Add CSIR header to admin login"
    git push origin feature/admin-login-header

Then open a Pull Request to csir-custom on GitHub for review.
## 6. Optional: Feature Branches + PRs

For larger changes, create a feature branch:

# Create branch from csir-custom
    git checkout csir-custom
    git pull origin csir-custom
    git checkout -b feature/admin-login-header

# Work, then save
    git add .
    git commit -m "Add CSIR header to admin login"
    git push origin feature/admin-login-header

Then open a Pull Request to csir-custom on GitHub for review.
## 7. Security & Housekeeping

❌ Do not commit secrets (passwords, tokens, DB creds).

✅ Respect `.gitignore.`

Add local editor/OS files
e.g.   `.vscode/`, `.idea/`, `.DS_Store`) if missing.

📝 Keep commit messages clean and meaningful.
## 8) Quick Command Cheat Sheet

# i. First time
    git clone https://github.com/PaakowTronics/limesurvey-csir.git
    cd limesurvey-csir
    git checkout csir-custom

# ii. Daily
    git pull origin csir-custom

# iii. To Save work
    git add .
    git commit -m "Describe changes"
    git push origin csir-custom

# iv. Conflicts (fix in VS Code)
    git add .
    git commit -m "Resolve merge conflicts"
    git push origin csir-custom

# v. (Advanced) Sync with upstream (if asked)
    git remote add upstream https://github.com/LimeSurvey/LimeSurvey.git
    git fetch upstream
    git checkout csir-custom
    git merge upstream/master
    git push origin csir-custom
## 9. Contact

Ping [@PaakowTronics](https://github.com/PaakowTronics) for branch policy or upstream sync questions.