1. What did --global mean here? What would happen if you left it out?
    Ans: It applies my name and email settings across all Git repositories on my system.
         Git applies the settings locally to only the current repository I am in. Other Git repositories on my machine will not inherit these settings.

2. What appeared in ls -a but not in ls? What is inside it?
    Ans: ls -a showed: .  ..  .git  .gitignore  README.md  lab-2  lab4  week-01  week-02  week01  week02
            ls showed: README.md  lab-2  lab4  week-01  week-02  week01  week02
         What appeared in ls -a but not in ls: The .git directory (and .git-related hidden items like .gitignore)
    
3. Roughly how many files and folders is Git offering to track? Does anything in that list look like something you did not write?
    Ans: Roughly how many files and folders is Git offering to track: 1 folder (lab-2/).
         Does anything in that list look like something you did not write: No.

4. Compare this git status with the one from Question 3. What disappeared?
    Ans: Nothing disappeared.

5. .gitignore itself shows up as untracked. Should it be committed, or ignored too? Why?
    Ans: It should be committed. Why?
         - Committing .gitignore ensures that everyone collaborating on the project automatically ignores the same junk files (like .venv/, __pycache__/, or system files) without needing to set up their own ignore rules manually.   
         - Git tracks .gitignore just like any other project source file so that its settings are saved and versioned along with my code.

6. README.md moved from one heading to another in the git status output. Which two? In the three-places model from the session, what just happened to it?
    Ans: It moved from Untracked files (or Changes not staged for commit) to Changes to be committed.
         It moved from the Working Directory to the Staging Area (Index).

7. What did Git print after the commit? How many files did it say changed?
    Ans: [master (root-commit) 1073aae] Lab work so far
         3 files changed, 1018 insertions(+)
         create mode 100644 .gitignore
         create mode 100644 lab-2/lab2_cc_2026.ipynb
         create mode 100644 lab-2/lab2_cc_2026.ipynb:Zone.Identifier

         1 file changed.
        
8. What are the first seven characters of your commit called, and what are they for?
    Ans: The first seven characters of your commit are called the Short Commit Hash (or Short SHA / Short SHA-1).
         What they are for:
         - They act as a unique reference or "fingerprint" for that specific commit in my repository.
         - Easy Reference: Instead of typing or copying the full 40-character SHA-1 hash, I can use these first 7 characters with Git commands to   identify and interact with that commit.

9. You now have two commits. Without looking it up: what are the four steps of the loop you just did twice?
    Ans: The four steps of the loop (the edit-stage-commit cycle) are:
         - Edit / Create: Make changes to your files or create new files in your working directory.   
         - Status: Run git status to see what changes were made and what files are untracked or modified.   
         - Stage: Run git add <file> to move the changes you want to save into the staging area.   
         - Commit: Run git commit -m "message" to create a permanent snapshot of those staged changes in your repository history. 

10. Why does this file get a special name and a special place, rather than being called notes.md like everything else?
    Ans: Here is why README.md gets a special name and place in the root folder:   
         - Standard convention: README is a universally recognized standard across software development and platforms like GitHub, GitLab, and Bitbucket.   
         - Automatic rendering: Platforms automatically look for README.md in the root directory of a repository and display its contents as the main homepage/documentation for the project.   
         - First point of contact: Keeping it in the root folder named README.md ensures anyone opening your project immediately sees an overview, setup instructions, and table of contents before diving into subfolders. 

11. What did gh auth login do that means you will not be asked for a password when you push?
    Ans: Running gh auth login authenticates your computer with GitHub and stores a secure personal access token (or SSH key) in your system's credential manager. Because Git is configured to use the GitHub CLI as its credential helper, whenever you run git push, Git automatically uses this stored token to authenticate you seamlessly in the background without needing you to type your password every time.

12. Refresh the repository page on GitHub. What is showing on the front page, and why that file?
    Ans: I see READEME.nd
    Automatic Rendering: GitHub is built to automatically search for a file named README.md in the root folder of any repository and render its Markdown formatting as the project's landing page.
    Standard Project Homepage: It serves as the front documentation for your repository, giving visitors an immediate summary, instructions, and overview of your work without them having to click into subfolders.

13. Run git log --oneline again. Did pushing change your local history in any way?
    Ans: No, pushing did not change your local history.

14. Your repository is private but your TAs can now read it. In your own words, what is the difference between a repository being private and a repository not existing on GitHub at all?
    Ans: A private repository exists on GitHub's servers and holds all your files and commit history, but access is restricted so only you and the specific collaborators you invite (like your TAs) can see or interact with it.
    If a repository does not exist on GitHub at all, there is no remote copy on the web—your code lives solely on your local computer, and no one else can view, clone, or access it through GitHub.
