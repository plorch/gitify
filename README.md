# gitify
getting git set up for workflow and project management

## Sources 

Using these sources for making this a more regular part of my workflow.

* https://happygitwithr.com/big-picture.html has some great R focussed advice including step by steps
    * This one has detailed steps based on different hardware
    * I cannot get SSH methods working, 
        * but after re-installing Git for Windows, got https credential cashing working
* https://openscapes.github.io/series/github-pub.html has some incomplete instructions and rationale and pholosophy
    * "Lab" culture
    * Code of conduct advice
    * other indoctrination

    
## Testing issues for project management
      
I am particularly interested in using Issues to see what they can do.

## Steps for starting a new gitified project

### Alternative 1:  Starting with GitHub repo (GitHub first)

1. Create new repo on GitHub with README.md or .Rmd for R projects

2. Copy https path

3. Alternatives:

	1. In git bash window navigate to where you want repo and type 

		* `git clone https://pathcopied_from_GitHub/reponame`

	2. In Rstudio

		* File -> New Project -> Version Control -> Github repo
		* Paste in path
		* Change directory location to one not already controlled by git
		* Tick Open new session


### Alternative 2:  Starting with an existing R project

1. If it is a local Git repo already or is in a directory that is (CMPCameraMonitoring) move critical files to a safe place

2. Remove the directory

3. In gitbash cd to the location just above where the dir sat and `git worktree prune`

4.  Create new repo on GitHub with README.md or .Rmd for R projects

5. Upload R files to GitHub

6. Set up a clone locally as in Alternative 1 above

### Alternative 3:  Starting with an existing R project

1. Make sure you have enabled git for R studio

2. Follow instructions for `usethis` in Happy Git with R instructions

** This has failed multiple times when I try adding existing dirs with `usethis` **

** Adding a project to an existing directory does not offer the make git repo checkbox **


## Push changes back to GitHub

* In Rstudio projects, this can be done from within Rstudio
* For non-R projects use 
	* git client like Gitcracken or 
	* git command line from inside local git repo
		* `git add -A`
		* `git commit -m "Useful commit message"`
		* `git push`

