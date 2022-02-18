# Demonstration of Git

This Repository is used as a Demo repository that I will be accessing from VS Code for learning all about Git.

## What is Git?
Git is a free open source distributed version control system for tracking changes in source code during software development. 
By version control we mean the ability to track changes in the source code of a program, and to merge those changes with changes from other sources, and to create a new version of the program. This is a method programmers use to keep track of their work/changes.

### CLoning a Repository to our local Machine
git clone < use either the HTTPS or SSH url (available in Github) >

### To see the hidden files 
Use la for Mac
Use ls -la for Windows

                HERE WE WILL FIND A FILE .git THIS BASICALLY SAVES ALL THE THE CHANGES/COMMITS THAT WE MADE IN GITHUB.com


#### Git Commands

1. git status
This shows all of the files that were updated, deleted or created but havent been saved in a commit yet.

2. git add
This method will help to track those files that was just created. So git needs to track the file before saving it to Git.
In most cases we use git add . --> This will tell to track all the files that are modified/untracked.
After this our files are ready to be committed.

3. git commit
This is the command to commit the files. We need to give <git commit -m "Some Message">
This will only save the files locally it is not live on Github yet.

4. git push
This will push the files to a remote repository where the project is hosted.
Before this we need to have an SSH key set up in our local device.
    We can use --> ssh-keygen -t rsa -b 4096 -C "<email>"

After this the key will be generated. Inorder to search for the key try <ls | grep <keyname>>
Now we have got 2 keys. One is the Public Key (which has .pub) the other is the private key.
The Private key will be the proof that you are infact the one who has generated the Public key.
In order to view the public key try: <cat <keyname.pub>>

Copy this and paste on Github Settings > SSH Key > Add New Key.

After this start ssh agent in the background using -> eval "$(ssh-agent -s)"
Try this: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection
                                                                
                                                                IF THIS FAILS
try < git remote add origin <HTTPS URL>>
Then try <git remote -v>

Then push to github using git push origin. This will have a pop-up window that you need to copy the url from and paste in VS Code.