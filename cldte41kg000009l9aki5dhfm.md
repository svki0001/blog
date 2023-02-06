# Git Branching Strategy

# Git Flow

Projects can be developed using Git with the following flow:

![The entire Git Flow (PR = Pull Request)](https://cdn.hashnode.com/res/hashnode/image/upload/v1675722239644/9a7188b0-575e-4df0-be63-92d46b0383a8.png align="center")

# Branches

* `feature branch`: For each task started, a new branch is created from dev. As soon as the task is completed, a pull request is created for this feature branch in the dev branch. Feature Branches are named by: \[task number\]-\[task title\], e.g. *11-simulation-widget*
    
* `dev`: The current development state. New branches for tasks are forked from this branch.
    
* `stage`: An intermediate state for testing and demos of new functions. So other stakeholders can have a look at a demo version.
    
* `hotfix`: Hotfixes are corrections that have to be published as soon as possible. After a hotfix is ready, it is merged into all three branches (`dev`, `stage`, `main`). Hotfix branches are named after hotfix-\[title\], e.g. *hotfix-video-crashing-on-reload*
    
* `main`: Published versions. The main branch represents the version that will be released to users.
    

Branch order

The order to merge the branches is as follows:  
`dev ➡️ stage ➡️ main`

The `stage` branch can be used for testing. If everything looks good, the tested `stage` is merged into the `main` branch via a pull request.

# Versioning

Versions are named according to the following pattern:  
`[MAJOR].[MINOR].[PATCH]`

1. `MAJOR` versions are fundamental changes. These include changes that fundamentally change the overall look and feel for the user, or make a large part of the code not backward compatible with older parts of the source code (e.g. change in software architecture).
    
2. `MINOR` versions are additional features that do not affect other parts of the source code, or affect them only slightly and are therefore backward compatible.
    
3. `PATCH` versions contain minor changes and bug fixes.
    

More info (e.g. pre-release) can be added via the tags in GitHub.