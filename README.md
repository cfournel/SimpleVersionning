SimpleVersionning
=================

A hook script to increment a version number for git


Design your own versionning schema like this : 

```bash

0.1
0.0.1
0.0.0.1

```

The code will auto-increment the version each time you commit files and will auto add to commit the version file




#Installation#

##1) Copy precommit file into your hook dir ##

in your git directory ( .git at your project root directory ), find the directory named "hooks".
Copy precommit into this dir.

##2) Create a version file##

Create to your root directory a file named "version.md" ( You can rename it as you want , but you will need to edit precommit script to match your version file ).
Write into your new fresh version file a starting version number like examples above.

NB : Version file should only contain number and dots, not words.

##3) Start commiting your codes !##

You will notice each time you commit, version.md ( or your custom version file ) is added to your commit.




#Next features#

Options to create a Git tag on each major updates following a schema like : 

0.0.9 -> 0.1.0 // No tag 0.1.0
0.9 -> 1.0 // Creation of tag 1.0
0.0.0.9 -> 0.0.1.0 // No tag 0.0.1.0
0.9.9.9 -> 1.0.0.0 // Creation of tag 1.0.0.0