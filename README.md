# Storm-API-Guide
## Reason for this existing?
This guide will be a starter guide on what to do when you begin using the Storm API since you will have to do some different things then if you were creating a Lua mod for Project Zomboid.
## Getting Started:
These are the steps you will need to do so you can get started.
* The first step you are gonna need to do is follow the instruction in the [Example Mod](https://github.com/mlem/storm/tree/docs/example-mod/example-mod) to create a example project in Intellij.
## Utilizing the Code?:
There are multiple things I can show you that will help you when trying to learn the difference between Lua and Java modding, but the biggest one is that you don't need to use the GlobalObject which is what is what allows you to do perform getSpecifiedPlayer(0) to get the player, instead you can just do ```IsoPlayer player = IsoPlayer.getInstance();``` since Project Zomboid Java side uses instances for most of everything going on. I would say around 90% of the time if you are looking for something that is currently running in the game, you can find it by getting the instance of the class.

There are two different ways you will normally have to get an instance in the Project Zomboid code, it will either by performing InsertClass.getInstance() or InsertClass.instance. You have to check both ways because sometimes the instance is private, which makes you have to use the getter for it. But if not then you can just perform the instance call straight to the declared variable.

//#TODO LEARN HOW TO ADD YOUR ITEMS TO THE GAME WITHOUT HAVING TO USE LUA SCRIPTS
