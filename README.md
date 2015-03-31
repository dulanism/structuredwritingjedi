# structuredwritingjedi
Readmes, tutorials and examples for structured tech writing

===

...before you do anything, know this:

## Git Commit Instance

Here's a use case for a folder I created called `dulanisdocs`, where I store my documentation edits and re-writes. Nest anyway as you please. I have sub-folders for each of the repos I contribute to.


1. After you get into the folder `dulanisdocs` create a new folder for the repo you want to update:
`mkdir -p <foldername>` (ex. `mkdir -p media-systems-web-assets`)
2. Then `cd <foldername>` (ex. `cd media-systems-web-assets`)
3. Then `git clone git@github.com:natgeo/media-systems-web-assets .`
4. In this instance, the `media-systems-web-assets` repo defaulted to `$ media-systems-web-assets git: (master)`. Don't work in the master branch. Instead:
	* add a new branch with this command: `git branch docs`
	* then switch to the branch by this command: `git checkout docs`
	* make sure your command line says `$ media-systems-web-assets git: (docs)`
5. Now you're in branch you created for that repo. Either use the command line or go your Finder and locate the folder `docs` (in my instance, `dulanisdocs` > `media-systems-web-assets` > `docs`)
	* Find/Open the file you need to edit. (In my instance I will open up the README file and edit with my changes)
6. When changes are made go back to the command line and `git add .`
7. Then you will commit with a short sentence on what your did with this command: `git commit -m "<your message in 72 characters>"`. Example (`git commit -m "Add table of contents to README"`).
8. Updates will be reflected in the repo, review and add a message in the larger field explaining your commit message and why, the save (i.e. 'Create Pull Request'). Keep the message short.
9. Then push the edits to the branch you created: `git push origin docs` (Note: If you created your own branch, for instance `newdocs`, the command will be `git push origin newdocs`).
10. Since you're working your own branch finalize the pull request with this command: `git pull origin docs`


## Recap after you mkdir
1. `cd media-systems-web-assets`
2. `git clone git@github.com:natgeo/media-systems-web-assets .`
3. `git branch docs`
4. `git checkout docs`
5. Go into `docs` folder on the branch of the same name
6. Make edits to the file in need
7. `git add .`
8. `git commit -m "<your message in 72 characters>"` (e.g. `git commit -m "Add video player instance to README"`)
9. `git push origin docs`
10. `git pu11 origin docs`

And the rest is up to the merge master.
