DayZ Chernarus Krona Castle Base For Console and PC xml json Mod Instructions & Terms Of Use

Limited Testing on PC Chernarus Local Server DAYZ Version 1.15 Nov 2021.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

Many Thanks To Inclement Dab for his amazing DayZ Editor that makes this all possible: https://steamcommunity.com/sharedfiles/filedetails/?id=2250764298

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "krona-castle-base.json" from the extracted files to inside the "custom" folder of the mission directory on your server. This file places the structures on your map.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "objectSpawnersArr" line.

This file tells your server to access your custom file.

Edit it to look like this: 

	"objectSpawnersArr": ["custom/krona-castle-base.json"],
	
If you already are calling custom jsons to spawn items, seperate the files like this:

	"objectSpawnersArr": ["custom/krona-castle-base.json","custom/differentfile.json"],
	
Save your changes & upload if you need to.
	
Next we add loot to the structures by adding the following code snippet to the top of your mapgrouppos.xml file, after <map> 

	<!--Krona Castle Base-->
	<group name="Land_Wreck_Ikarus" pos="1431.798950 302.360016 9289.446289" rpy="-1.978822 -0.034068 81.854004" a="8.146"/>
	<group name="Land_Wreck_S1023_Blue" pos="1436.060059 302.177429 9283.249023" rpy="-0.000000 -0.000000 -177.104095" a="-92.8959"/>
	<group name="Land_Wreck_hb01_aban1_green" pos="1440.530029 301.915009 9278.950195" rpy="0.000000 0.000000 122.561989" a="-32.562"/>
	<group name="Land_Wreck_hb02_aban1_black" pos="1444.510010 296.911011 9286.309570" rpy="0.000000 27.999998 -98.650688" a="-171.349"/>
	<group name="Land_Wreck_sed01_aban1_police" pos="1440.859009 301.593079 9275.610352" rpy="-0.000000 -0.000000 119.478951" a="-29.479"/>
	<group name="Land_wreck_truck01_aban1_orange" pos="1446.579956 300.058014 9269.940430" rpy="0.000000 -15.000000 138.339005" a="-48.339"/>
	<group name="Land_Medical_Tent_Shower" pos="1425.176147 303.092865 9293.825195" rpy="-0.000000 -0.000000 -126.078156" a="-143.922"/>
	<group name="Land_Medical_Tent_Big" pos="1429.135010 309.211060 9253.827148" rpy="-0.000000 -0.000000 56.557468" a="33.4425"/>
	<group name="Land_Wall_Gate_FenG_Big" pos="1421.581909 302.175598 9297.928711" rpy="-0.000000 -0.000000 -41.546856" a="131.547"/>
	<group name="Land_Mil_Fortified_Nest_Small" pos="1413.763428 302.498413 9307.370117" rpy="-0.000000 -0.000000 -36.520519" a="126.521"/>
	<group name="Land_Mil_Tent_Big1_1" pos="1392.065552 304.869629 9319.804688" rpy="-0.000000 -0.000000 0.000000" a="90"/>
	<group name="Land_Mil_Tent_Big2_5" pos="1413.381836 310.644623 9260.225586" rpy="-0.000000 -0.000000 157.439270" a="-67.4393"/>
	<group name="Land_Mil_Tent_Big1_1" pos="1395.790039 303.061005 9300.129883" rpy="0.000000 -4.000000 -107.370003" a="-162.63"/>
	<group name="Land_Mil_Tent_Big2_3" pos="1376.079956 294.191986 9316.169922" rpy="-2.200000 0.000000 0.000000" a="90"/>
	<group name="Land_Misc_Toilet_Mobile" pos="1421.301392 310.611969 9253.337891" rpy="-0.000000 -0.000000 143.375351" a="-53.3754"/>
	<group name="Land_Misc_Toilet_Mobile" pos="1422.690186 310.533447 9254.100586" rpy="-0.000000 -0.000000 143.375351" a="-53.3754"/>
	<group name="Land_Misc_Toilet_Dry" pos="1359.522705 293.109161 9317.985352" rpy="-0.000000 -0.000000 0.000000" a="90"/>
	
Save your changes & upload if you need to.

Restart your server and the new structures will appear immediatly, and then they will slowly stock with loot.

Thanks, Rob.
