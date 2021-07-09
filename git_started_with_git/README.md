
# Command line basics 
  
- **ls** - On Macs, lists the current files within your current directory
- **mkdir name-of-directory** - make a new directory (folder)
- **touch name-of-file** - On Macs, make a new file
- **cd ./other-directory** - Change directory into the one you want by providing the path to that directory, for example:
- **cd ..** - go out one level from your current directory (remember the space)

We will now show you how to create a new repl! 

## Instructions


1. List the files in your current directory to see what's there. What's in there? You'll see one file there which was auto-generated when you created the repl
2. Create a directory called **my-directory** using the instructions above.
3. List the files in your current directory again - what’s new?
4. Create a file called **my-file.md**
5. List your files again - what’s new?
6. Make another directory
7. List all your files again, what has changed?
8. Change directory into either directory by providing the path to that directory
9. List the files, what's inside?
10. Change directory by going one level out of the directory back to where you started.

-------

## Introducing and using Git 
 

Why use Git?

- We just made 2 new directories and a new file. Let's run 'git status' to see what the current state is in our terminal. 

- We need to initialise Git before it starts to track changes.

- Run **'git init'** then run **'git status'**. What do you see now?

- When files show up as **'Untracked files'** it means they are not saved.

- Let's save the new directories and the file now by doing a Git commit. This is essentially the same as when you save a document on word etc.

To commit all the files, first we need to add them by running: 
**git add name-of-file**

- Run **git status**, what has changed?

Tip: You can add all new files at the same time by running **git add .** 

- To commit the files we've added we need to run:
**git commit -m 'our description of what we are saving**

You might get an error asking for you to set your account's identity before you can commit, follow the instructions in the terminal, you will need to enter each of the following separately: 

**git config --global user.email youremail@whatever.com** 

**git config --global user.name your-name**

- Once you've added the above you should be able to commit. 

- Run git status - if you get:
**On branch master
nothing to commit, working tree clean** then you can move on!

Tip: Run **git log** to look at your commit history! 

- Now that everything is saved locally in our environment (we're using repl.it now but usually we'd be using git on our own machines), what happens if repl.it breaks or if we lose our laptops? We have no back-up if everything is saved locally... 

This is where GitHub comes in handy! 

## Introducing and using GitHub 

Git allows us to save things and track changes locally, GitHub allows us to save remotely (in the cloud) and displays what we've saved using Git in a nicer way! We can access Github from anywhere that we have access to the internet. 

There are also a bunch of cool features on GitHub that help developers collaborate.

#### Pushing to GitHub
- Go to GitHub, click on your repositories and then the **'new'** green button. Name your repo, click **'public'** then **'create repository'**
- Next you'll need to create a [Personal Access Token](https://github.com/settings/tokens) to use instead of your GitHub password in Replit
- Follow the instructions under **…or push an existing repository from the command line**
> git push
Username for 'https://github.com': your-username
Password for 'https://katerina-codes@github.com': token-generated-from-GitHub 
- You've now just made your first push to GitHub, go ahead and take a look on GitHub, you should see your files on there now.

#### Pulling Changes from GitHub
Now let's make a change on GitHub and try to pull that back to our local machine. This might simulate a colleague making some changes to the code that you're both collaborating on, they've pushed them to the remote repo and you want to bring those changes to your local copy.

Every GitHub repository should have a file called README.md. It's the file that is automatically shown to everyone visiting your project and is used to tell other devs what your code does and how to use it. The `.md` extension 
- Go to GitHub and click the `Add a README` button
- Change the markdown text in the editor from `# github-test` to something like `# Welcome to my first GitHub Repo`.
- Scroll down and add a commit message such as 'Created README file'
- Click `Commit changes`

Now those changes are stored remotely on GitHub, but how do we pull them back down to your local machine?
- You can check to see if commits have been made remotely with the command `git remote show origin`
- Pull those changes with `git pull`
- You should now see the README.md file in the file structure on the left.

Congratulations, you've just made your first pushes and pulls to and from GitHub! Go ahead and spend some time now adding to your README file with some of the things you've learnt from this workshop and try pushing those updates to your GitHub repo.
