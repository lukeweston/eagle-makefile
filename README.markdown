
Makefile for Eagle projects.

Usage: The makefile is invoked in the directory containing the project.brd and project.sch pair of eagle files.

The makefile is edited with the appropriate PROJECT_NAME variable. (Need to improve this so it's more user friendly, possibly by checking the directory name.)

Prerequisites: git, eagle and gerbv installed. Eagle must be in the path so it can be executed from shell.

You'll need a GitHub account - and you'll need to edit the makefile with your username and API key.

At the moment this creates an open-source GitHub repository - if you desire a private GitHub repo you can probably modify the API call to do this.


What it does:

- Generates Gerber files for PCB fabrication.
- Generates a preview rendering of the PCB as a PNG image, using gerbv.
- Generates a template README.markdown containing a link to the image in the GitHub repo, and the project name, if none exists already.
- Checks everything into a git repository, creating a new repository if it doesn't already exist.
- Builds a GitHub repository if it doesn't already exist.
- Pushes the local git repository to GitHub.

So, just run make, and your Eagle PCB layout is converted into standard Gerber files, with a image rendering generated, committed into a local git repository for
version control and backup, and it is (by default) pushed up onto an open-source GitHub repository so it can be shared with the world, and it all happens quickly and easily
without any effort required at all. Neat, huh?

