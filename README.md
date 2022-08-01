# Custom SLD Sets for Cockatrice
Currently, the cards.xml file used by [Cockatrice](https://github.com/Cockatrice/) to display card images lumps all the Secret Lair Drops together into one set (SLD) and Cockatrice only shows art for the most recent SLD printing of a card as a result of this. This makes sense from a clerical perspective, as Wizards of the Coast also considers all the Drops to be a single set.

However, this makes it impossible to choose which art to use for cards printed in several Drops (like Sol Ring) and very difficult to choose whether to use the Secret Lair art or the normal art for cards on a Drop by Drop basis unless you do some very specific and tedious prioritizing.

This repository contains separate .xml files for most of the Secret Lair Drops, to allow for more fine-grained art choice. These can be dropped into the Custom Sets Folder and then prioritized to your liking like any other real set. 

# How to Use
Card Sets:

1) Download the .xml's for the sets that you want
2) Place them in the 'customsets' folder for Cockatrice (Card Database -> Open Custom Sets should take you right there)
3) Change the 'xx' in each file name to some unique two digit number, with a leading zero if necesary (01, 02, 03, etc)
4) Restart Cockatrice and confirm the enabling of new sets
5) Prioritize the new sets as needed in Card Database -> Manage sets...

Token Sets:

1) Download the token .xml file included with the set release
2) Open the 'customsets' folder for Cockatrice (Card Database -> Open Custom Sets should take you right there)
3) Copy the set and card information from the token file into the TK.xml file in 'customsets' and save the file
4) Restart Cockatrice.

Souce: The wonderful [Cockatrice Wiki](https://github.com/Cockatrice/Cockatrice/wiki/Custom-Cards-&-Sets)

# Drops NOT in this Repository
Drops that are entirely multiple artworks for the same card:
* Bitterblosom Dreams
* Foil Jumpstart Lands
* Happy Little Gathering
* Mother's Day 2021
* Mountain, Go
* Persistant Petitioners
* Seeing Visions
* Thalia - Beyond the Helvault

Cockatrice will only display one piece of artwork for a card at a time so it doesn't make sense to have a custom set that is only one card with multiple artwork lines. If you want a particular piece of art for a card from one of these sets, better to just add it to the [CUSTOM folder](https://github.com/Cockatrice/Cockatrice/wiki/Custom-Cards-&-Sets) in Cockatrice.

Drops that aren't in Cockatrice cards.xml currently:
* Stranger Things
* Secret Lair x Fortnite
* Secret Lair x Fortnite: Locations

# Making Your Own

You are welcome to use my SLD_split() function (listed above) to make your own custom sets by pulling cards out of the SLD set. It will work on any list of card names from SLD. Just be careful what you name the set so as not to overlap with the 4-letter codes used in Cockatrice already. The function will check if the code entered is already in use to a point; it only looks at codes that end in 'D' since I name all my Drop sets with a 'D' at the end. Also ensure that the function has pulled to correct version of the card that you want; it ouputs a list of collector numbers you can compare to Scryfall for this purpose. You may need to manually change the UUID in the .xml file if not. I make the occasional token file manually, so no code is provided for that.
