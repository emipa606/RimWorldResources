# My update-workflow for mods to 1.1

- Assemblies
If the mod does not come with Source-files, use dnSpy or similar to extract the files from the Assemblies.

https://rimworldwiki.com/wiki/Modding_Tutorials/Decompiling_source_code#Decompiling_source_code

* Open the solution

* Update the framework to 4.7.2
![framework](https://raw.githubusercontent.com/emipa606/RimWorldResources/master/Images/framework.png)

* Set the output-path to a 1.1-directory if you want to support 1.0 and 1.1
![output](https://raw.githubusercontent.com/emipa606/RimWorldResources/master/Images/output.png)

* References usually needs to be updated 
![references_old](https://raw.githubusercontent.com/emipa606/RimWorldResources/master/Images/references_old.png)

* UnityEngine should be replaced with UnityEnginge.CoreModule, also other modules if the mod uses them.

* All game-references are located in the the game folder RimWorld\RimWorldWin64_Data\Managed

* If the game uses Harmony or HugsLib, use NuGet to install the latest version.
![nuget_start](https://raw.githubusercontent.com/emipa606/RimWorldResources/master/Images/nuget_start.png)
![harmony](https://raw.githubusercontent.com/emipa606/RimWorldResources/master/Images/harmony.png)

* Go through all references and verify that the "Copy Local"-flag is set to false.

* Then try to build the solution and see what errors pup up.
