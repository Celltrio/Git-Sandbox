## Git Exercise
- This is a practical exercise to learn Git.
- Before you begin the exercise, make sure you have the following setup on your system
  - Git application installed
    - Git Desktop (Windows GUI Application) - Simple
    - TortoiseGit (Windows File Manager integrated) - Moderate
    - Git for Windiows (Windows CMD application) - Complex
    - VS Code (Development studio with Git integration)
  - You have an active account on GitHub for Celltrio
    - https://github.com/orgs/Celltrio/
    - Repository: Git-Sandbox
  - You have cloned the "Git-Sandbox" repository
    - git clone https://github.com/orgs/Celltrio/Git-Sandbox

## The Exercise
- You have been tasked to help populate the CellTrio training forest.  We will need you to add trees (documents) to the forest (Folder) and create Git branches to populate our training repository.  Please ensure your Git environment has been setup before you begin the exercise.
- This is a self paced exercise that should not take you more than 15-20 minutes to complete.  Should you have any questions, please consult your favorite LLM (AI) or one of the SystemEngineering team members who have completed the exercise.  You can find a list of these members in the Forest\README.md file

### Start Exercise
1. Navigate to the Git-Sandbox folder
2. Switch to the "develop" branch
   - git switch develop
3. Create a new branch for your exercise in the format <initials>-Tree-Exercise
   - git checkout -b abc-Tree-Exercise
4. Navigate to the Forest folder, and copy the Template-tree.txt file to a new text file <initials>-tree.txt
   - cd Forest
   - copy "Template-tree.txt" to "abc-tree.txt"
5. Edit your new file, and add a "leaf" to "Branch-B" of the tree
   - Notepad abc-tree.txt
   - type: <Leaf-001>
   - Save the file
6. Commit the changes you have just made to your branch
   - git status - to see files that have changed
   - git add <files> - any files listed in the status
   - git commit -m "added my first leaf" - commit the changes with a message
7. Edit the tree file to add a few more leaves (at least 3) to any of the three branches (A, B, or C)
   - Open file (if not already open) abc-tree.txt
   - type 3-4 lines: <Leaf-00X>
   - Save the file
8. Commit the changes you have just made to your branch
   - git status - to see files that have changed
   - git add <files> - any files listed in the status that have changed
   - git commit -m "added more leaves to my tree" - commit the changes with a message
9. Edit the tree file and remove one of the leaves (Fall has arrived)
   - Open file (if not already open) abc-tree.txt
   - locate a leaf delete it from the leaf line of a branch
   - Save the file
10. Commit the changes you have just made to your branch
   - git status - to see files that have changed
   - git add <files> - any files listed in the status that have changed
   - git commit -m "removed leaves from my tree" - commit the changes with a message
   - close your editor
11. Now push your changes to GitHub and prepare a Pull Request (PR) to add your changes to the 'develop' branch
   - git push
   - From GitHub:
     - locate your branch, notice it indicates changes have been made
     - create the Pull Request (PR) and make a comment about what have done
     - select a an experienced team member to be a reviewer
     - activate the new PR
12. Once the reviewer has approved the PR, merge the PR
   - From GitHub:
     - press the Merge button
     - allow the merge to delete your branch, or delete your branch from GitHub      
13. Back on your local file system, update your repository to sync with GitHub
   - git switch develop
   - git pull
14. Verify that your changes are in the "develop" branch, and remove your exercise branch
   - Open your editor and your tree file abc-tree.txt
     - your changes should still be in place as you had left them 
   - git branch -D abc-Tree-Exercise

## End of Exercise
