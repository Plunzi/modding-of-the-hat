THE DEFINITIVE GUIDE FOR

![img](https://github.com/Plunzi/modding-of-the-hat/blob/main/wiki-images/clip_image002.gif?raw=true)


SCRIPT/FUNCTIONALITY MODDING 



# MODIFYING **GAME SCRIPTS**

The awesome 🔗 **King of the Hat Community** found out how to mod the game from the code side of the game. Instead of replacing assets such as characters & portraits. We can replace and potentially add new code!

_**Note**: In this document we will use "KOTH" as short version for "King of the Hat"_

## How To Guide
This tutorial will be rather **DIFFICULT** because no Modloader for KOTH has been finished yet. the 🔗[ModTheHat Modloader](https://github.com/ModTheHat/ModTheHat) is in the working though. Once it is done you will be informed here asap! Basically the Modloader will be able to mod the game by creating **C# .DLL files** using Visual Studio or any other C# Editor of your choice. which the Modloader injects into the game.

This tutorial will show you how to modify the game files **DIRECTLY**.
### Chapter 1: Dependencies for manual modding
You will need the following:

🔗 [dnSpy - Programm](https://github.com/dnSpy/dnSpy/releases/tag/v6.1.8)

With dnSpy you can access more like KOTHs source scripts and asset files. Download **dnSpy** by downloading the binaries from the GitHub releases page.

Extract it and open **dnSpy**.

### Chapter 2: OPENING FILES
In **``dnSpy clic File``** 🠖 **``Open``** _(Alternatively CTRL + O)_

![](https://github.com/Plunzi/modding-of-the-hat/blob/main/wiki-images/Aspose.Words.12e64fed-b1a9-4767-b0a5-7e5bf1e1730a.001.png)

And navigate to your installation of King of the Hat. In the game folder, open the file in **``KingOfTheHat\_Data/Managed/Assembly-CSharp.dll``**
![](https://github.com/Plunzi/modding-of-the-hat/blob/main/wiki-images/Aspose.Words.12e64fed-b1a9-4767-b0a5-7e5bf1e1730a.002.png)

Inside dnSpy you can find **ALL** of the classes the game uses.
### _(OPTIONAL)_ Chapter 3: Removing Hat hunters!

Expand these folders,
**``Assembly-CSharp/Assembly-CSharp.dll/``**

this is how it should look like

![](https://github.com/Plunzi/modding-of-the-hat/blob/main/wiki-images/Aspose.Words.12e64fed-b1a9-4767-b0a5-7e5bf1e1730a.003.png)

Find the file**``(technically class)`` **Release.
Search for **``HAT\_HUNTERS\_DEFAULT``** until you see a line that looks like this

![](https://github.com/Plunzi/modding-of-the-hat/blob/main/wiki-images/Aspose.Words.12e64fed-b1a9-4767-b0a5-7e5bf1e1730a.004.png)

Right click and click on Edit Method

![](https://github.com/Plunzi/modding-of-the-hat/blob/main/wiki-images/Aspose.Words.12e64fed-b1a9-4767-b0a5-7e5bf1e1730a.005.png)

and then replace **``flags[ReleaseFlag.HAT\_HUNTERS\_DEFAULT];``** with **``‘false;’``**
after doing so click on **``Compile``**

![](https://github.com/Plunzi/modding-of-the-hat/blob/main/wiki-images/Aspose.Words.12e64fed-b1a9-4767-b0a5-7e5bf1e1730a.006.png)

**NOTE:** This does not set your game to always do Last Hat Standing yet. This is because the game loads Flags from **``KingOfTheHat\_Data/Managed/StreamingAssets/ReleaseToggles.json``**, therefore find **``HAT\_HUNTERS\_DEFAULT``** and set Release and Experimental to **``false``**.

```json
{
	"flag": 1006,
    "name": "HAT_HUNTERS_DEFAULT",
	"Experimental": false,
    "Release": false
}
```
But this chapter still shows you how to modify ANY part of the game.
### Chapter 4: Saving your changes.
Click on **``File``** and then **``Save All…``**

![](https://github.com/Plunzi/modding-of-the-hat/blob/main/wiki-images/Aspose.Words.12e64fed-b1a9-4767-b0a5-7e5bf1e1730a.008.png)

Finally click on Ok

![](https://github.com/Plunzi/modding-of-the-hat/blob/main/wiki-images/Aspose.Words.12e64fed-b1a9-4767-b0a5-7e5bf1e1730a.009.png)

Great, you made it mate! 😎
Have fun with your modified game.

## Community made mods
Currently there are no community made mods, as soon as there are any we will list them here.
If you made one suggest a change for this document here at our GitHub page, thanks❤️.

