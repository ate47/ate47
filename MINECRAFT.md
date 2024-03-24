[Go back](https://github.com/ate47)

# Information about my Minecraft Mods

You can read this page as a FAQ

**Table of content**

- [Information about my Minecraft Mods](#information-about-my-minecraft-mods)
  - [Disclaimer](#disclaimer)
  - [Can I help?](#can-i-help)
  - [When does version X get published?](#when-does-version-x-get-published)
  - [Can the mod X can be made for the modloader Y?](#can-the-mod-x-can-be-made-for-the-modloader-y)
  - [The mod can work by simply updating the Minecraft version](#the-mod-can-work-by-simply-updating-the-minecraft-version)
  - [How does the version system works?](#how-does-the-version-system-works)

## Disclaimer

I'm not playing Minecraft anymore, so my will to do mods on this game is very low.

## Can I help?

Yes! You can fork a repository containing the mod/plugin you want to work on and create a pull request. I will review the code and if everything is ok, I will upload it on CurseForge / Modrinth / SpigotMC to let everyone access your work.

## When does version X get published?

If I have the time and some motivation, I will update the mod to the latest version, but this is purely random (look at this [mod](https://www.curseforge.com/minecraft/mc-mods/gm3-teleporter/files) for example) so I can't answer this question.

## Can the mod X can be made for the modloader Y?

Usually X = [Advanced Creative Tab](https://github.com/ate47/AdvancedCreativeTab) and Y = [Fabric](https://fabricmc.net/)

Converting a mod from a mod loader to another can be, depending on the size and the calls to the mod loader API, long and annoying. Adding to that the [disclaimer](#disclaimer) and the answer is probably never.

## The mod can work by simply updating the Minecraft version

If this is true, you can fork the repository of a mod, update the fabric.mod.json (**Fabric**) or the mods.toml (**Forge**) and then create a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) with the update, I check if I can launch it and publish the result on CurseForge/Modrinth.

## How does the version system works?

This system is close to the [semantic versionning](https://semver.org/).

versions are named like that: X.Y.ZW

- With invisible small changes in the code itself or fixes: Z++
- Visible changes, new functions or deprecated functions: Y++
- Huge changes, rebase of the code: X++
- ``W`` can be omitted, it describe an alpha state ``a`` or a beta state ``b``, release is omitted

