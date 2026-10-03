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

