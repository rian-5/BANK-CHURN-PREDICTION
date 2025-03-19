---
# GUIDE FOR TEAM MEMBERS 

## Overview
This project uses a  Bank churn Kaggle dataset stored in **Google Drive** for easy access by all team members. We will work collaboratively using **Google Colab** notebook.

## HOW TO USE THIS GITHUB REPOSITORY AS A TEAM

Open google colab https://colab.google/

Open  a new notebook

Inside the first colab code cell Run:
```sh
!apt install git

# Change to your working directory
%cd /content

# Clone the shared GitHub repository
!git clone https://github.com/Adamsomondi/BANK-CHURN-PREDICTION.git

# Move into the repo
%cd BANK-CHURN-PREDICTION

# Checks the contents of the repository
!ls -la

# Ensures you are in the correct repository
%cd /content/BANK-CHURN-PREDICTION
```

## HOW TO USE THE DATASET AS A TEAM

 Insert a new second colab code cell then Run:
 ```sh
 import pandas as pd

# Correct direct file link
file_id = "1-6FhvYRRgceTptrIMfgvaXkq-QKw8dwf"
file_url = f"https://drive.google.com/uc?id={file_id}"

# Load the dataset
df = pd.read_csv(file_url)

df
```

## HOW TO WORK ON YOUR OWN NOTEBOOK 

Before this rename your notebook to what you are working on i.e edaanalysis.ipynb,Datacleaning.ipynb<b> don't leave it to untitled.ipynb</b>

 ### Create a New Branch: 
 
 Each team member should create their own branch to work on their notebook. This helps in keeping the main branch clean and allows for easy merging of changes.

 Insert a new third cell and run:
 
 ```sh
 #Replace you-branch-name with what you are working on i.e edaanalysis,datacleaning etc..
 !git checkout -b your-branch-name
  ```

## Copy the colab  file to your working directory

Replace the datacleaning.ipynb with the  file you are working i.e edaanalysis.ipynb etc..

Insert a third cell and run:

```sh
from google.colab import drive
drive.mount('/content/drive')

!ls -la "/content/drive/My Drive/Colab Notebooks"
!find "/content/drive/My Drive" -name "Datacleaning.ipynb"

!cp "/content/drive/My Drive/Colab Notebooks/Datacleaning.ipynb" /content/BANK-CHURN-PREDICTION/

!ls -la "/content/BANK-CHURN-PREDICTION/"
```

## WORK ON YOUR NOTEBOOK

The work is allocated according to each Person according to every Milestones.Every person Creates their notebook and works on it,Save it so we move
To different milestone easily.

You should be able to make sure you push the correct work.
 
# After working on your notebook

 Insert a fourth cell and run:
 
```sh
# Git commands to push the changes adding your changes
!git config --global user.name "Adamsomondi" #replace your own github name.
!git config --global user.email "mustafajohnson123@gmail.com" #replace your own github gmail.
!git add .

 # Commit your changes
!git commit -m "Updated data cleaning" #write a message "finished data Cleaning/added eda analysis"
```

 ## Push Your Branch
 
 Before you push your branch to the remote repository.

Generate a PAT Token,

Go to your GitHub Developer Settings. https://github.com/settings/tokens

Click on Generate new token the Token(classic one).

Select the scopes or permissions you need, such as repo for full control of private repositories.

Click Generate token and copy the token. You will not be able to see it again, <b>so save it securely</b>.

 Set the Remote URL to Use HTTPS

Insert a fifth cell and run:

 ```sh
#!git remote set-url origin https://<TOKEN>@github.com/Adamsomondi/BANK-CHURN-PREDICTION.git  #replace <TOKEN> with PAT keys you created.
!git remote set-url origin https://the token@github.com/Adamsomondi/BANK-CHURN-PREDICTION.git #replace the token with what you copied
```

**Push Your Branch Using HTTPS**

```sh
!git push origin your-branch-name # Replace with your actual branch name you created earlier
```

 ## Create a Pull Request
 Once you are ready to merge your changes into the main branch, create a pull request on GitHub. This allows other team members to review your work before it is merged.
 
Go to the Repository on GitHub

Navigate to the repository on GitHub (https://github.com/Adamsomondi/BANK-CHURN-PREDICTION).


Switch to Your Branch from github

Switch to the branch you just pushed by selecting it from the branch dropdown menu.

Create a Pull Request

 ## Reviewed and Merged
   Other team members should review the pull request. Once it is approved, it can be merged into the main branch
  
 ---
 
# BANK-CHURN-PREDICTION
## Milestone 1

![Screenshot](https://github.com/Adamsomondi/BANK-CHURN-PREDICTION/blob/main/images/Screenshot%202025-03-19%20031243.png)













