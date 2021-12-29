# Yourvisit
This project is to collect information about different places across the world (DEMO ONLY)

# How to Contribute?
The codebase is maintained using the "contributor workflow" where everyone without exception contributes patch proposals using "pull requests" (PRs). This facilitates social contribution, easy testing and peer review.

To contribute a patch, the workflow is as follows:

1. Fork repository (only for the first time)
2. Create topic branch
3. Commit patches

# Refactoring 

Refactoring is a necessary part of any software project's evolution, however Pull requests that refactor the code should not be made by new contributors.
It requires a certain level of experience to know where the code belongs to and to understand the full ramification (including rebase effort of open pull requests).

# Testing
Testing and code review is the bottleneck for development; we get more pull requests than we can review and test on short notice. Please be patient and help out by testing other people's pull requests.

# Automated Testing
Developers are strongly encouraged to write unit tests for new code, and to submit new unit tests for old code.

# QA Testing
Changes should be tested by somebody other than the developer who wrote the code. This is especially important for large or high-risk changes. It is useful to add a test plan to the pull request description if testing the changes is not straightforward.

# Commiting Updates
In general, commits should be atomic and diffs should be easy to read. For this reason, do not mix any formatting fixes or code moves with actual code changes.
Make sure each individual commit is hygienic: that it builds successfully on its own without warnings, errors, regressions, or test failures.

# Pull Requests

The title of the pull request should be prefixed by the component or area that the pull request affects. Valid areas as:

CO - Country Name
ST - State Name
DT - District Name

Eg- If you updating something from Bangalore, Mention "IN-BLR-HEB"

# Squashing your commit 

If your pull request contains fixup commits (commits that change the same line of code repeatedly) or too fine-grained commits, you may be asked to squash your commits before it will be reviewed. The basic squashing workflow is shown below.

      git checkout your_branch_name
      git rebase -i HEAD~n
          #n is normally the number of commits in the pull request.
          #Set commits (except the one in the first line) from 'pick' to 'squash', save and quit.
          #On the next screen, edit/refine commit messages.
          #Save and quit.
      git push -f # (force push to GitHub)

# Rebasing 
When a pull request conflicts with the target branch, you may be asked to rebase it on top of the current target branch. The git rebase command will take care of rebuilding your commits on top of the new base.

This project aims to have a clean git history, where code changes are only made in non-merge commits. This simplifies auditability because merge commits can be assumed to not contain arbitrary code changes. Merge commits should be signed, and the resulting git tree hash must be deterministic and reproducible. 

# Decision Making 

# Peer Review

# backporting 

Security and bug fixes can be backported from master to release branches.
A backport should contain the following metadata in the commit body:

Github-Pull: #<PR number>
Rebased-From: <commit hash of the original commit>
