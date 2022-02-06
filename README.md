# common-cube
Custom common cube cards to be used in Cockatrice

Set-up Guide
1) Clone the Repo
2) Open Cockatrice
	2.1) Card Database -> Open custom image folder
	2.2) Copy "Common_Cube_Custom_Set_Cockatrice_Pics" folder into the folder that just opened
	2.3) Card Database -> Open custom sets folder
	2.4) Copy "Common_Cube_Custom_Set_Cockatrice.xml" into the folder that just opened
3) Restart Cockatrice
4) To verify the changes have taken effect search for "Ajani's Mantra" and check that the card has the custom text (2 instances of graft 1)
5) If you see the normal "Ajani's Mantra" go to Card Database -> Manage sets
	5.1) Make sure that the "Common Cube" set is at the top of the list
	
Update Cockatrice with new edits:
1) git pull
2) Remove "Common_Cube_Custom_Set_Cockatrice_Pics" folder from your "custom image folder"
3) Remove "Common_Cube_Custom_Set_Cockatrice.xml"  from your "custom sets folder"
4) Repeat Set-Up Guide.

Making new edits:
1) Open "Common_Cube_Only_Edits.mse-set" in MSE (Magic Set Editor)
2) Add the new editted card.
3) Get the new xml
	3.1) In MSE File -> Export -> HTML
	3.2) Select "Cockatrice" from the list
	3.3) Use the following parameters for the export
		Version: CS/ECH 1.04
		Usage Guide: Https://tinyurl.com/csexporter
		Cockatrice Set Type: custom
		Export Images: No (will will do this step manually for just the edited cards later)
		Images File Type: JPG*
		Tokens In Separate XML: No
		Append Set Code To Tokens: No
		Append String To Names: BLANK*
		Include Common: Yes
		Include Uncommon: Yes*
		Include Rare: Yes*
		Include Mythic: Yes*
		Include Basic Land: Yes*
		Include Tokens: Yes*
		Include Special: Yes*
		
		Items with * don't matter
		
	3.4) Click "OK"
	3.5) Save to the location of your repo using the name "Common_Cube_Custom_Set_Cockatrice.xml" replacing the existing file
4) Add new card images
	4.1) File -> Export -> All Card Images
	4.2) Use the following parameters
		Format: {card.name}.png
		Handle Duplicating filenames: Overwrite Old Files
		Cards to export: Entire Set
	4.3) Click "OK"
	4.4) Go into "Common_Cube_Custom_Set_Cockatrice_Pics" in your local repo and click "Save"
5) Open git bash in the location of your local repo
6) git checkout -b myname-branch
7) git add Common_Cube_Custom_Set_Cockatrice.xml
8) git add Common_Cube_Custom_Set_Cockatrice_Pics
9) git commit -am "Add new edits for CARDNAME,CARDNAME,..."
10) git push origin myname-branch

How to play:
I have made a Cube Cobra list here: https://cubecobra.com/cube/list/61ffd44c477ed80fb175d065
However, Cube Cobra does not support custom cards. Fortunately many of our editted cards have the same name so building your deck in cockatrice is easy.
For the cards with custom names use this spread sheet to find it's common cube counterpart name: https://docs.google.com/spreadsheets/d/1sWagcxX9HO7A3T_juhTTKU1Z_5V6eQNAg9rNaZ-cVTE/edit?usp=sharing
While drafting, you will not see the cards with their custom effects. To do so you can always look up their image in the "Common_Cube_Custom_Set_Cockatrice_Pics" folder.