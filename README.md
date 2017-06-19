# Silver Steel

> A freelance spy is a great job. It pays well and you get to travel to new and interesting places. Unless you get caught, that part is not so great.
> You open the unmarked envelope and unfold the mission briefing enclosed within: *Infiltrate MegaCorp, gain access to the data centre, download the database.*
> So here you are, standing in the foyer of MegaCorp, disguised as a repairman.

Silver Steel is a spy themed interactive fiction story.


# License

See file COPYING for the source code license.

## Releasing

Release steps include tagging the current version and building a new website.

* Generate release notes

  git log CURRENT_VERSION_TAG..HEAD --oneline >> CHANGES

* Edit CHANGES
* Update the release number in the story
* Build a z8 file into the Materials directory
* Build a blorb package (this includes the z8 from above as a download link in the website)
* git add . && git commit -m "Update release version"

* Tag the new version

  git tag -a NEW_VERSION

* Push changes and tags

  git push origin --tags

## Website

* checkout gh-pages
* cp -r "Code Name Silver Steel.materials/Release/*" .
* git add . && git commit -m "Build"
* git push && git checkout master

