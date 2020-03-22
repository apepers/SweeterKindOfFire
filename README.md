# SweeterKindOfFire
Twine project to convert Sweeter Kind of Fire into an interactive experience

# Installing Tweego
If you want to be able to switch between the Twine editor and working in code, you'll need Tweego.
To install it and automatically add it to your path, following the installation instructions here:
https://github.com/ChapelR/tweego-installer

# Quick local previewing
If you want to preview the game locally without having to push, you can do that quickly as long as you've installed Tweego as above.
Open a command line terminal inside of the repo folder (for example, `C:\Users\Alexei\Documents\Github\SweeterKindOfFire`) and run the following command:

`tweego SweeterKindOfFire.twee -o SweeterKindOfFire.html`

You can then navigate to the repo folder and double click `SweeterKindOfFire.html` to open it in your web browser and play your modified version to test.

Github will notice that you've modified the html file when you go to commit your changes. You can commit if you want, but it will re-compile the html anyway based on the twee, so you can safely revert the html file instead and just commit your twee file. Either works.

You also have access to some extra functionality when testing this way.
## To preview your changes with testing enabled (aka same as Test in the Twine editor)
`tweego SweeterKindOfFire.twee -o SweeterKindOfFire.html -t`

## To start at a different passage than the normal start
As an example, to start as the passage named 'PickDrink'

`tweego SweeterKindOfFire.twee -o SweeterKindOfFire.html --start=PickDrink`

Note that if the passage name has spaces you will need quotes

`tweego SweeterKindOfFire.twee -o SweeterKindOfFire.html --start="Cheap wine"`

## To detect new changes without needing to rebuild
You can put Tweego in a 'watch' mode which will cause it to rebuild every time you save the twee file, updating the html file. This lets you simply make a change, save it, and refresh your local version of the game to see it in action.

Note that when you refresh it does remember what passage you were on, so this can be really handy to fix typos as you see them.

To run in watch mode, use

`tweego SweeterKindOfFire.twee -o SweeterKindOfFire.html -w`

# How to edit in the Twine editor
If you want to switch to working in Twine so you can visualize your work, you can use the SweeterKindOfFire.html file automatically generated in the repo. Simply import that file into Twine or copy-paste it into your Twine story folder, and start editing.

# How to convert back into Twee and commit
If you've made changes in Twine that you now want to commit, you will need to convert those changes back into a Twee file. You'll need to have installed Tweego with the instructions above.

You will need to know the path to your Twine stories (where your modified HTML file will be with the edits you've made in Twine), and the path to the repo where you need to update the Twee file.

If we open a command line inside of our repo folder (for example, `C:\Users\Alexei\Documents\Github\SweeterKindOfFire`) then we will not need to specify an extra folder location for the Twee file, just the Twine file.

If our Twine file is located at `C:\Users\Alexei\Documents\Twine\Stories\SweeterKindOfFire.html` then run the command:

`tweego -d C:\Users\Alexei\Documents\Twine\Stories\SweeterKindOfFire.html -o SweeterKindOfFire.twee`

You should then be able to open the twee file and verify your changes have been copied over. You can also examine in the diff in git. If anyone else has changed the story while you were working, at this point you could pull and merge the changes with the twee file. If everything looks good, you're ready to push and it will automatically update the html in the repo to use the new twee!

