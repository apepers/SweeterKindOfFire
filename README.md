# SweeterKindOfFire
Twine project to convert Sweeter Kind of Fire into an interactive experience

# Installing Tweego
If you want to be able to switch between the Twine editor and working in code, you'll need Tweego.
To install it and automatically add it to your path, following the installation instructions here:
https://github.com/ChapelR/tweego-installer

# How to edit in the Twine editor
If you want to switch to working in Twine so you can visualize your work, you can use the SweeterKindOfFire.html file automatically generated in the repo. Simply import that file into Twine or copy-paste it into your Twine story folder, and start editing.

# How to convert back into Twee and commit
If you've made changes in Twine that you now want to commit, you will need to convert those changes back into a Twee file. You'll need to have installed Tweego with the instructions above.

You will need to know the path to your Twine stories (where your modified HTML file will be with the edits you've made in Twine), and the path to the repo where you need to update the Twee file.

If we open a command line inside of our repo folder (for example, `C:\Users\Alexei\Documents\Github\SweeterKindOfFire`) then we will not need to specify an extra folder location for the Twee file, just the Twine file.

If our Twine file is located at `C:\Users\Alexei\Documents\Twine\Stories\SweeterKindOfFire.html` then run the command:

`tweego -d C:\Users\Alexei\Documents\Twine\Stories\SweeterKindOfFire.html -o SweeterKindOfFire.twee`

You should then be able to open the twee file and verify your changes have been copied over. You can also examine in the diff in git. If anyone else has changed the story while you were working, at this point you could pull and merge the changes with the twee file. If everything looks good, you're ready to push and it will automatically update the html in the repo to use the new twee!

