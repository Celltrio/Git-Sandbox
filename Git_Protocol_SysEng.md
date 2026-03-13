# Git Workflow Document - Systems Engineering
## Protocol Description
- This protocol is to be used when executing operations in Git
  - The operations to be performed
    1. The repository Branches
    2. The Development Workflow
    3. Sharing files with others
  - Setup your local Git application
    - Git Desktop
    - Tortise Git
    - Git for Windows (Command Line, and GUI)
    - VS Code
    - Visual Studio (vs2022, vs2026)
    - Other
  - I will provide the protocol from a command line perspective.  You will need to translate the command into you GUI application framework.  All of the operations are available in all the tools listed above.  Ask your favorite LLM for assiatance in using your GUI application if you need help.

## The Repository Branches
- See full repository figure above.
- Branches
  - main
    - The base branch of the repository. 
    - It is only to be used for releases (DO NOT COMMIT any changes directly to this branch)
    - Changes to this branch will only be Releases of the documents
    - The latest stable release will be the HEAD of this branch
  - develop
    - The primary working branch for the team
    - All changes to this branch will be from a branch merge (PR - Pull Request)
    - Direct changes to this branch are only to resolve conflicts.
    - The latest unstable release will be the HEAD of this branch
  - features/improvement/bug
    - These branches will made from the 'develop' branch
    - These branches should only have a lifetime while the change is being developed
    - Once the change is ready for acceptance, it should be merged into 'develop' with a (PR)
    - These branches must be kept up to date with other changes in 'develop' (sync)
      - periodically, merge 'develop' into these branches; fix conflicts, and commit to this branch
    - Before merging back into 'develop', (sync) the branch to 'develop'
      - Delete this branch (GitHub and local) after merging
  - Release_x.x.x
    - These branches are created from 'develop' when a candidate is ready for release
    - Regression testing and Validation will be performed on this branch
    - Bugs found in testing will be commited to this branch directly
      - checkout this branch, create a new branch from it, make changes, merge back into this branch (PR)
    - When this branch is ready for release
      - Merge this branch (PR) into 'main'
      - Tag the 'main' branch with a Release tag (GitHub)
      - Merge this branch (PR) into 'develop'
        - resolve any conflicts on this branch before completing the merge
      - Delete this branch (GitHub and local) after merging
  - Patch_x.x.x.y
    - These branches are created from 'main' when a patch of a release is necessary
    - Regression testing and Validation will be performed on this branch
    - The changes to the branch will be made directly on this branch
    - When this patch is ready for release
      - Merge this branch (PR) into 'main'
      - Tag the 'main' branch with a Release tag (GitHub)
      - Merge this branch (PR) into 'develop'
        - resolve any conflicts on this branch before completing the merge
      - Delete this branch (GitHub and local) after merging

## The Development Workflow

## Sharing Files

# Appendix
## Creating a new Repository
### New Repository
1. Create your initial file(s) in a folder location on your PC
  a. C:\\Users\\<name>\\Documents\\repos\\SandBox\\myFile.txt
2. Open your Git application
3. Create a new local repository
  - git init
  - git add .
  - git commit -m "Add: Initial commit of files/folders"
  - On GitHub:
    - Create a new Repository
      - Make the new repository Public
      - DO NOT add a README file
    - Copy the repo URL
  - git remote add origin <repo URL>

### Existing Repository
1. git clone <repo>
  - ex. git clone https://github.com//Celltrio/Git-Sandbox.git

## Prepare the Repository
1. Create the 'develop' branch
  - git checkout -b develop
2. Make a simple change to an existing file, or create a new file
  - Edit somefile.whatever
3. Commit the change to the develop branch
  - git status  //Show files that have changed
  - git add <file(s)>
  - git commit
4. Push the develop branch to GitHub
  - git push origin develop
