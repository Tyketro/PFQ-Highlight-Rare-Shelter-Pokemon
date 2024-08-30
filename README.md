Rare Pokémon Glow in Shelter (For PokéFarm Q)

What does this script do?
This script will add a coloured back shadow to certain Eggs & Pokémon while in the Shelter. Different categories of Pokémon get different coloured shadows.

This script does NOT affect parties, fields or the Pokédex. Only the Shelter.

NOTE: Currently the script only supports Regular sprites. No Shiny, Albino or Melanistic. QOL has a built-in highlight feature for these, which are a lot less subtle. Mini-sprites are not currently supported.

QOL Required
QOL Userscript is required for this script. You can activate it by going to Farm > Options > Userscripts, and then checking the box next to QOL.



HOW TO INSTALL:
This script requires no downloading, but it does require copy and pasting. It is recommended you use this on a computer, rather than a phone or tablet.

1. Start by opening the link to the script that you want to use. (Combined is the recommended script)

2. On the GitHub page, click on the code, then highlight all text (Ctrl+A) and copy it (Ctrl+C).

3. Go back to Pokearm and open up the QOL menu, which is usually found on the end of your Timers Bar.

4. Scroll down until you see "Css Settings", click on the large text box underneath this title.

5. Create a new line, and then paste. (Ctrl+V)

6. Refresh the page (F5), and the script should now be working! Go check the Shelter to see :)



HOW TO CUSTOMISE:
I wanted to add some instructions to help you customise the script!

Visuals

For customising the glow itself, everything you need is located towards the end of each script section, marked by:
/* End of [Section] highlight in Shelter */

Shortly above it, you will find a line that looks like this:
filter: drop-shadow(5px 5px 5px #3802f7);
(There are additional comments surrounding this, that also explain what it is.)

Customising the glow, only requires you to change what is in the brackets.

Horizontal Offset
The first figure adjusts how far from the sprite the shadow is horizontally. By default it is 5px.

Vertical Offset
The second figure adjusts how far from the sprite the shadow is vertically. By default it is 5px.

Blur
The third figure adjusts how blurred the glow is. The higher the number, the more blurry and subtle it gets. By default it is 5px.

Glow Colour
The fourth figure adjusts the colour of the glow. In the example and script I am using HEX colour code, which I would recommend.
Use a colour picker (Google will have one if you search for it), and once you have selected a colour you want to use, click and copy the HEX value, and paste it over the figure currently present. All HEX code will be a hashtag followed by 6 characters.



Customising the Pokémon Involved

This will be more complex, and require you to edit the code.
Every img has a comment next to it, labelling what the img is corresponding to. Every img has its own line in the script. It is important to know which lines you will be editing.


Delete an image from the script:

Once you have found the Pokémon you want to remove, highlight the entire line and delete it. If this is the last line of the section, please make sure that the new line that ends the section has no comma (,) after the ] , otherwise the script will stop working.


Adding an image to the script:

Decide which section to add a Pokémon to. Then go to the last img entry of that section, and add a comma (,) after the ] in that entry.
Go to the end of that line, after the comment, and then press Enter to start a new line.
Copy and paste in this code:
&[src*="pkmn/IMG.png"]

Replace the IMG with the img code of the sprite you wish to add. the PFQ Wiki will list all of these under the "List of Pokémon pages." They will look something like this 8/v/i/3 and can range from 2 to 4 characters.
If you are adding multiple images, please ensure all have a comma (,) and the ] EXCEPT the final entry, otherwise the script will break.
I also recommend adding a comment stating what img you have added in between /* and */ so that you know if you need to revisit the code.



Q&A
Here's some Questions and Answers which hopefully makes some queries about the scripts clearer to you.


Q: Can I change the colour of the glows?
A: Yes, you can! Above is a hide box that contains a tutorial on how to do this, as well as change the size and blur.


Q: Does the order in the Combined script matter?
A: Kinda. In CSS, the latter scripts take priority over the scripts before it. Some Pokémon will fill multiple criteria. I've ordered it so that more important criteria are prioritised as such, whilst still leaving the Pokémon in the other scripts so that users can choose what they want it to appear. e.g. Raging Bolt is Legendary & Paradox; Paradox is prioritised.


Q: Why is Legendary here when it already has a highlight option in QOL?
A: This was more down to personal preference. Compared to what I would usually use the QOL highlight feature for, I found it too distracting for how common Legendary Pokémon can be in the shelter, and I wanted a more subtle option.


Q: Why aren't Mega Evolutions in this list?
A: Mega Evolutions are already highlighted appropriately by the QOL highlight feature. As of right now I have made scripts for categories of Pokémon that had no highlight option, or in Legendary's case were too prominent in their highlights.

