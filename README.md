# Storm-API-Guide
# Table of Contents
1. [Reason for this existing?](#reason-for-this-existing)
2. [Adding to this knowledge?](#adding-to-this-knowledge)
3. [Getting Started?](#getting-started)
4. [Utilizing the Code?](#utilizing-the-code)
5. [Instance Use](#instance-use)
6. [Item Creation](#item-creation)
7. [Drawing Text](#drawing-text)
## Reason for this existing?
This guide will be a starter guide on what to do when you begin using the Storm API since you will have to do some different things then if you were creating a Lua mod for Project Zomboid.
## Adding to this knowledge?
You can add a Pull Request at any time and as long as it is something that builds upon the knowledge already added then it will be accepted.
## Getting Started?
Luckily actullay getting started isnt that hard since we have our god Mlem who spent his hard time making a example mod for the Storm API community (He is also the person who maintains the currently used versions of Storm API, so fr pray to him).

You can find his example project [here](https://github.com/mlem/storm/tree/docs/example-mod/example-mod).
## Utilizing the Code?
### Instance use:
There are multiple things I can show you that will help you when trying to learn the difference between Lua and Java modding, but the biggest one is that the Java side of Project Zomboid uses instances to access everything being used in the game at the moment.

For example you don't need to use the LuaManager.GlobalObject which is what is what allows you to do perform getSpecifiedPlayer(0) to get the player, instead you can just do ```IsoPlayer player = IsoPlayer.getInstance();```.

I would say around 90% of the time if you are looking for something that is currently running in the game, you can find it by getting the instance of the class.

There are two different ways you will normally have to get an instance in the Project Zomboid code, it will either by performing InsertClass.getInstance() or InsertClass.instance. You have to check both ways because sometimes the instance is private, which makes you have to use the getter for it. But if not then you can just perform the instance call straight to the declared variable.
### Item creation:
Lua Scripts... :(

At this point in time I am still trying to learn how to add items to the game the same way the PZ devs do it, but once I do figure that out you can bet I will be adding it to this repo.

If anyone knows how PZ adds items to the game Java side then please make a pull request with some information on how to do it.

//#TODO LEARN HOW TO ADD YOUR ITEMS TO THE GAME WITHOUT HAVING TO USE LUA SCRIPTS
### Drawing text:
You can draw text to the screen relatively easily in Project Zomboid. All you have to do is call the ```TextManager.instance``` which allows you to perform the ```DrawString(font, x, y, text, 1.0, 1.0, 1.0, 0.7);``` method.
- font = The font you wish to use when drawing the text, you can get the UI font by performing ```UIFont.FontSize``` where in the FontSize you can choose between Small, Medium, or Large.
- x = Where on the x-plane you wish to start rendering your text.
- y = Where on the y-plane you wish to start rendering your text.
- text = The string you wish to draw on the screen.

//#TODO ADD WHAT ALL THE VARIABLES IN DRAWSTRING METHOD MEAN
