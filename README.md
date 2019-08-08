#####################################
# Good Reference
#####################################
https://www.analyticsvidhya.com/blog/2018/05/starters-guide-jupyter-notebook/
https://github.com/kb22/Coursera_Capstone


On the Mac:

#####################################
# Create an SSH key
#####################################
$ ssh-keygen -t rsa -b 4096 -C "zhjohn925@hotmail.com"

Enter file in which to save the key (/Users/zhjohn/.ssh/id_rsa): /Users/zhjohn/.ssh/id_rsa_hotmail

#####################################
# Add the SSH key to the ssh-agent
#####################################
$ eval "$(ssh-agent -s)"


# Check if your .ssh directory contains a file named config. if not,
# then create one and name it config (with no extension). Add the below lines
# in config. Please note all the lines except the first one are indented.

Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa_hotmail
 
# Finally, add the key to the agent by running the following in Terminal:

$ ssh-add -K ~/.ssh/id_rsa_hotmail

#####################################
# Add the Key to Your Github Account
#####################################

# Copy the public version of your key to the clipboard buffer:

$ pbcopy < ~/.ssh/id_rsa_hotmail.pub

# Go to your Github account, and click your profile picture in the top right corner 
# of your Github account and select “Settings”.
# Under Personal settings, select “SSH and GPG keys”.
# Click the button "New SSH Key" and paste a new SSH key to your account.

#####################################
# Create a Github Repository
#####################################
# You can create a new repository is by clicking the “+” sign next to your profile pic and 
# selecting “New repository” from the drop-down menu

